<template>
  <view class="upload-case">
    <view class="upload-case-cont">
      <AtForm>
         <picker
          class="upload-case-cont-picker"
          mode='selector'
          :range="selector"
          :value="selectorValue"
          @change="handleChange"
          @cancel="handleCancel"
          >
            <view class='demo-list-item'>
              <view class='demo-list-item__label'>相关停车场</view>
              <view class='demo-list-item__value'>
                {{ selector[selectorValue] }}
              </view>
          </view>
        </picker>
        <picker
          class="upload-case-cont-picker"
          mode='multiSelector'
          :range="multiSelector"
          :value="mulitSelectorValues"
          @change="handleMulitChange"
          @columnchange="handleColumnChange"
          >
            <view class='demo-list-item'>
              <view class='demo-list-item__label'>案件类型</view>
              <view class='demo-list-item__value'>
                {{
                  `${
                  multiSelector[0][mulitSelectorValues[0]]
                } & ${multiSelector[1][mulitSelectorValues[1]]}`
                  }}
              </view>
          </view>
        </picker>
        <picker
          class="upload-case-cont-picker"
          mode='selector'
          :range="selector3"
          :value="selectorValue3"
          @change="handleChange"
          @cancel="handleCancel"
          >
            <view class='demo-list-item'>
              <view class='demo-list-item__label'>紧急程度</view>
              <view class='demo-list-item__value'>
                {{ selector3[selectorValue3] }}
              </view>
          </view>
        </picker>
      </AtForm>
    </view>
    <view class="upload-case-cont">
      <view class="upload-case-cont-bottom">
        <text class="bottom-title">附件</text>
        <text class="bottom-mintitle">可上传图片、视频、文件数量不超过8个</text>
      </view>
      <AtImagePicker
        :files="files"
        :onChange="onChange"
        :showAddBtn="true"
      />
    </view>
  </view>
</template>

<script>
import './upload-case.scss'
let Imgicon = require('../../assets/arrow-right.png')
import { AtForm, AtListItem, AtImagePicker } from 'taro-ui-vue'
export default {
  components:{
    AtForm,
    AtImagePicker,
    AtListItem
  },
  data () {
    return {
      value:"",
      imgIcon:Imgicon,
      selector: ['滨江停车场', '滨江停车场2', '滨江停车场3', '滨江停车场4'],
      selectorValue: 0,
      multiSelector: [
        ['饭', '粥', '粉'],
        ['猪肉', '牛肉']
      ],
      mulitSelectorValues:[0,1],
      selector3: ['一般', '紧急', '非常紧急'],
      selectorValue3: 0,
      files: [
        {
          url: '../../assets/demo.png',
        }
      ]
    }
  },
  methods: {
    handleClick () {
      this.msg = 'click button';
    },
    handleCancel(e) {
      console.log('handleCancel', e)
    },
    handleChange (e) {
      this.selectorValue = e.detail.value
    },
    handleMulitChange (e) {
      console.log('handleMulitChange', e)
      this.mulitSelectorValues = e.detail.value
    },
    handleColumnChange(e) {
      console.log('handleColumnChange', e)
    },
    onChange (files) {
      this.files = files
    },
    onFail (mes) {
      console.log(mes)
    },
    onImageClick (index, file) {
      console.log(index, file)
    }
  }
}
</script>
