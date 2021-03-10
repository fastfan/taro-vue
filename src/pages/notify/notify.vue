<template>
  <view class="index">
      <commonList :infoList="msgList"></commonList>
  </view>
</template>

<script>
import './notify.scss'
import  commonList  from '../../component/commonList/index.js'
export default {
  components:{
     commonList
  },
  data () {
    return {
      msg: '消息通知!',
      msgList:[
         {
           time:"2020年1月16日 09:19:30",
           icon:require("../../assets/demo.png"),
           title:"案件核实",
           cardNo:'736485937',
           request:"啊啊啊啊啊啊啊啊",
           finishTime:"2019-9-28"
         },
         {
           time:"2020年1月16日 10:19:30",
           icon:require("../../assets/demo.png"),
           title:"案件核实",
           cardNo:'736485937',
           request:"啊啊啊啊啊啊啊啊",
           finishTime:"2019-9-28"
         },
         {
           time:"2020年1月16日 10:19:30",
           icon:require("../../assets/demo.png"),
           title:"案件核实",
           cardNo:'736485937',
           request:"啊啊啊啊啊啊啊啊",
           finishTime:"2019-9-28"
         },
         {
           time:"2020年1月16日 10:19:30",
           icon:require("../../assets/demo.png"),
           title:"案件核实",
           cardNo:'736485937',
           request:"啊啊啊啊啊啊啊啊",
           finishTime:"2019-9-28"
         },
         {
           time:"2020年1月16日 10:19:30",
           icon:require("../../assets/demo.png"),
           title:"案件核实",
           cardNo:'736485937',
           request:"啊啊啊啊啊啊啊啊",
           finishTime:"2019-9-28"
         },
       ]
    }
  },
  methods: {

  }
}
</script>
