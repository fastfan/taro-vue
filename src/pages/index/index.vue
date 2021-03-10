<template>
  <view class="personal-center">
    <view class="personal-center-avater">
      <image :src="userInfo.imgIcon"  class="personal-center-avater-img"></image>
      <view class="personal-center-avater-text">
          <view class="userinfo-nickname">{{userInfo.nickName}}</view>
          <view class="userinfo-department">{{userInfo.department}}</view>
      </view>
    </view>
  </view>
</template>

<script>
import './index.scss'
let imgIcon = require("../../assets/demo.png");
export default {
  components:{

  },
  data () {
    return {
      msg: '个人中心!',
      userInfo:{
         imgIcon:imgIcon,
         nickName:"王渊铭",
         department:"沙雕部"
      }
    }
  },
  methods: {
    handleClick () {
      this.msg = 'click button';
    }
  }
}
</script>
