<template>
  <view class="example-case">
    <view class="example-case-cont">
        <AtSwipeAction autoClose :on-click="handleClick.bind(this,index)" v-for="(item,index) in caseList" :key="item.title+index" :options="item.options" :is-opened="item.isOpened">
           <view :class="[index===caseList.length-1?'example-case-cont-cont2':'example-case-cont-cont']">
              <view class='example-case-cont-cont-top'>
                <text class="top-left">{{item.title}}</text>
                <text class="top-right">{{item.date}}</text>
              </view>
              <view class='example-case-cont-cont-bottom'>
                <text class="bottom-left">{{item.case}}</text>
                <text class="bottom-right">{{item.pro}}</text>
              </view>
           </view>
        </AtSwipeAction>

    </view>
  </view>
</template>

<script>
import './example-case.scss'
import { AtSwipeAction } from 'taro-ui-vue'
export default {
  components:{
    AtSwipeAction
  },
  data () {
    return {
      msg: '个人中心!',
      caseList:[
        {
          title:"龙湖天街停车场",
          date:"1993-10-12 09:23",
          case:"故障-车位故障",
          pro:"非常紧急",
          options:[
            {
              text: '删除',
              style: {
                background:`url('../../assets/delete.png') #FF4949 center 22px no-repeat`,
                backgroundSize: '20px 20px',
              }
            }
          ],
          isOpened: false
        },
        {
          title:"龙湖天街停车场2",
          date:"1993-10-12 09:23",
          case:"故障-车位故障",
          pro:"非常紧急",
          options:[
            {
              text: '删除',
              style: {
                background:`url('../../assets/delete.png') #FF4949 center 22px no-repeat`,
                backgroundSize: '20px 20px',
              }
            }
          ],
          isOpened: false
        },
        {
          title:"龙湖天街停车场3",
          date:"1993-10-12 09:23",
          case:"故障-车位故障",
          pro:"非常紧急",
          options:[
            {
              text: '删除',
              style: {
                background:`url('../../assets/delete.png') #FF4949 center 22px no-repeat`,
                backgroundSize: '20px 20px',
              }
            }
          ],
          isOpened: false
        },
        {
          title:"龙湖天街停车场4",
          date:"1993-10-12 09:23",
          case:"故障-车位故障",
          pro:"非常紧急",
          options:[
            {
              text: '删除',
              style: {
                background:`url('../../assets/delete.png') #FF4949 center 22px no-repeat`,
                backgroundSize: '20px 20px',
              }
            }
          ],
          isOpened: false
        },
        {
          title:"龙湖天街停车场",
          date:"1993-10-12 09:23",
          case:"故障-车位故障",
          pro:"非常紧急",
          options:[
            {
              text: '删除',
              style: {
                background:`url('../../assets/delete.png') #FF4949 center 22px no-repeat`,
                backgroundSize: '20px 20px',
              }
            }
          ],
          isOpened: false
        },
        {
          title:"龙湖天街停车场2",
          date:"1993-10-12 09:23",
          case:"故障-车位故障",
          pro:"非常紧急",
          options:[
            {
              text: '删除',
              style: {
                background:`url('../../assets/delete.png') #FF4949 center 22px no-repeat`,
                backgroundSize: '20px 20px',
              }
            }
          ],
          isOpened: false
        },
        {
          title:"龙湖天街停车场3",
          date:"1993-10-12 09:23",
          case:"故障-车位故障",
          pro:"非常紧急",
          options:[
            {
              text: '删除',
              style: {
                background:`url('../../assets/delete.png') #FF4949 center 22px no-repeat`,
                backgroundSize: '20px 20px',
              }
            }
          ],
          isOpened: false
        },
        {
          title:"龙湖天街停车场4",
          date:"1993-10-12 09:23",
          case:"故障-车位故障",
          pro:"非常紧急",
          options:[
            {
              text: '删除',
              style: {
                background:`url('../../assets/delete.png') #FF4949 center 22px no-repeat`,
                backgroundSize: '20px 20px',
              }
            }
          ],
          isOpened: false
        },
        {
          title:"龙湖天街停车场",
          date:"1993-10-12 09:23",
          case:"故障-车位故障",
          pro:"非常紧急",
          options:[
            {
              text: '删除',
              style: {
                background:`url('../../assets/delete.png') #FF4949 center 22px no-repeat`,
                backgroundSize: '20px 20px',
              }
            }
          ],
          isOpened: false
        },
        {
          title:"龙湖天街停车场2",
          date:"1993-10-12 09:23",
          case:"故障-车位故障",
          pro:"非常紧急",
          options:[
            {
              text: '删除',
              style: {
                background:`url('../../assets/delete.png') #FF4949 center 22px no-repeat`,
                backgroundSize: '20px 20px',
              }
            }
          ],
          isOpened: false
        },
        {
          title:"龙湖天街停车场3",
          date:"1993-10-12 09:23",
          case:"故障-车位故障",
          pro:"非常紧急",
          options:[
            {
              text: '删除',
              style: {
                background:`url('../../assets/delete.png') #FF4949 center 22px no-repeat`,
                backgroundSize: '20px 20px',
              }
            }
          ],
          isOpened: false
        },
        {
          title:"龙湖天街停车场4",
          date:"1993-10-12 09:23",
          case:"故障-车位故障",
          pro:"非常紧急",
          options:[
            {
              text: '删除',
              style: {
                background:`url('../../assets/delete.png') #FF4949 center 22px no-repeat`,
                backgroundSize: '20px 20px',
              }
            }
          ],
          isOpened: false
        },
      ]
    }
  },
  methods: {
    handleClick (index) {
      this.caseList.splice(index,1)
    }
  }
}
</script>
