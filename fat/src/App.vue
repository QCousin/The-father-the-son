<template>
  <div id="app">
      <div class="header">
        <span  v-for="(item,index) in tabList" :key="index" @click="tabfn(index)" :class="{active:index==ind}">{{item.title}}</span>
      </div>
      <div class="main">
        <connect  v-for="(item,index) in tabList[ind].like" :key="index" :like="item"/>
      </div>
  </div>
</template>

<script>
import connect from './components/connect'

export default {
  name: 'App',
  components: {
    connect
  },
  data(){
    return {
      tabList:[
       {
         title:"七喜",
         like:"我要变好看",
        
       },
        {
         title:"李宛卿",
         like:"今生卖花，来世漂亮",         

       },
        {
         title:"心如止水",
         like:"不喜不悲",         

       }
       ],
       ind:0,
    }
  },
  methods:{
    tabfn(ind){
      this.ind = ind
      
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
span{
  padding:0 20px;
}
.active{
  color:blue;
}
.main{
  width:280px;
  height:360px;
  border:1px solid #ccc;
}
</style>
