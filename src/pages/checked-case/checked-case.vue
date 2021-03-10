<template>
  <view class="checked-case">
    <view>已核实案件</view>
  </view>
</template>

<script>
import './checked-case.scss'

export default {
  components:{

  },
  data () {
    return {
      msg: '已核实事件!',
    }
  },
  methods: {
    handleClick () {
      this.msg = 'click button';
    }
  },
  mounted(){

  }
}
</script>
