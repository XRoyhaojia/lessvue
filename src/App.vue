<template>
  <div id="app">
    
    
    <alertCom :title='title' :content='content' :cancelE='cancelE' :confirmE='confirmE' v-if='isok'></alertCom>
    
  </div>
</template>

<script>

import alertCom from './components/AlertCom';

export default {
  name: "App",
  data() {
    return {
      title:'小心路滑',
      content:'是否跳转到虎扑',
      isok:true
    }
  },
  components: {
 
    alertCom
  },
  methods: {
    cancelE:function() {
      this.isok = false;
    },
    confirmE:function() {
      location.href = 'https://www.hupu.com/';
    }
  },
};
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
