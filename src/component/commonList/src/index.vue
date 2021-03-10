<!--
 * @Author: fastfan
 * @Date: 2021-03-02 17:18:02
 * @LastEditors: fastfan
 * @LastEditTime: 2021-03-03 10:21:18
 * @Description: 通用列表
-->
<template>
  <view class="commonlist">
       <view v-for="(item,index) in infoList" :key="index" class="commonlist-cont">
          <view class="commonlist-cont-list">
            <text class="commonlist-cont-list-time">{{item.time}}</text>
            <view class="commonlist-cont-list-cont">
              <image class="commonlist-cont-list-cont-left" :src="item.icon"></image>
              <view class="commonlist-cont-list-cont-right">
                <text class="right-title">{{item.title}}</text>
                <view class="right-cont">
                   <text>您获派一个新的案件核实任务。案件编号：{{item.cardNo}},
                     核实要求：{{item.request}}。核实完成时间：{{item.finishTime}}。请尽快落实，谢谢！</text>
                </view>
              </view>
            </view>
          </view>
       </view>
  </view>
</template>

<script>
export default {
   name:"commonList",
   props:{
     infoList: {
       type:[Array],
       default:function(){
         return []
       }
     }
   },
   data(){
     return {

     }
   }
}
</script>

<style lang="scss">
  .commonlist{
    &-cont{
      &-list{
        text-align: center;
        margin: 24px 48px 24px 24px;
        &-time{
          font-size: 24px;
          font-weight: 400;
          color: rgba(0,0,0,0.25);
          text-align: center;
        }
        &-cont{
          display: flex;
          justify-content: space-between;
          margin: 24px 0 0;
          // align-items: center;
          &-left{
            width: 80px;
            height: 80px;
            margin: 15px 15px 0 0;
          }
          &-right{
            flex: 1;
            width: 296px;
            background: #fff;
            border-radius: 2px;
            box-shadow: 0px 2px 5px 0px rgba(221,221,208,0.30);
            text-align: left;
            padding: 30px;
            .right-title{
              font-weight: 500;
            }
            .right-cont{
               margin:16px 0 0 0 ;
               color: #333333;
               line-height: 44px;
               font-weight: 400;
            }
          }
        }
      }
    }
  }
</style>
