<template>
  <view class="task-center">
    <view class="task-center-top">
       <view class="task-center-top-cont">
         <text class="task-center-top-title">{{verifiedData.title}}</text>
         <view class="task-center-top-cont-center2" @tap="jumpTo(verifiedData)">
           <image class="task-center-top-cont-center-icon" :src="verifiedData.icon"></image>
           <view class="task-center-top-cont-center-text">{{verifiedData.name}}</view>
         </view>
       </view>
       <view class="task-center-top-cont">
         <text class="task-center-top-title">{{caseDataTitle}}</text>
         <view class="task-center-top-cont-block">
           <view class="task-center-top-cont-center" v-for="(item,index) in caseData" :key="index" @tap="jumpTo(item)">
             <image class="task-center-top-cont-center-icon" :src="item.icon"></image>
             <view class="task-center-top-cont-center-text">{{item.name}}</view>
           </view>
         </view>
       </view>
    </view>
    <view class="task-center-mid">
       <AtCard
        extra='查看全部'
        :title="'待核实事件 '+ '('+unChecked.num+')'"
        thumb='../../assets/case_edit.png'
        :onClick="cliclPanel"
      >
        <view class="task-center-mid-title">案件编号20200920</view>
        <view class="task-center-mid-contTop">
          <text class="task-center-mid-contTop-mintitle">故障-车位故障</text>
          <text class="task-center-mid-contTop-extra">非常紧急</text>
        </view>
        <AtDivider content='' />
        <text class="task-center-mid-cont">案件描述案件描述案件描述案件描述案件描述案件描述案件描述案件描述案件描述</text>
        <view class="task-center-mid-contBot">
          <text class="task-center-mid-contBot-text">滨江区停车场A</text>
          <text class="task-center-mid-contBot-time">2020-10-12 09:23</text>
        </view>
      </AtCard>
    </view>
  </view>
</template>

<script>
import './task-center.scss'
import { AtCard,AtDivider } from 'taro-ui-vue'
import Taro from "@tarojs/taro";
export default {
  components:{
     AtCard,
     AtDivider
  },
  data () {
    return {
      msg: '任务中心!',
      verifiedData:{
        title:"核实取证",
        icon:require('../../assets/checked.png'),
        name:"已核实事件",
        path:"checked-case"
      },
      caseDataTitle:"案件上报",
      unChecked:{
        num:3
      },
      caseData:[
        {
          icon:require('../../assets/checked.png'),
          name:"案件上报",
          path:"upload-case"
        },
        {
          icon:require('../../assets/case.png'),
          name:"案件草稿箱",
          path:"example-case"
        },
        {
          icon:require('../../assets/cased.png'),
          name:"已上报案件",
          path:"escalated-case"
        },
      ]
    }
  },
  methods: {
    cliclPanel () {
      console.log('点击了面板')
    },
    jumpTo(params){
      Taro.navigateTo({
        url: `/pages/${params.path}/${params.path}`
      })
    }
  }
}
</script>
