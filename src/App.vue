<template>
  <div id="app">
    <zhexiantu></zhexiantu>
    <zhuzhuangtu></zhuzhuangtu>
  </div>
</template>

<script>
import zhuzhuangtu from './components/zhuzhuangtu.vue'
import zhexiantu from './components/zhexiantu.vue'
export default {
  name: 'App',
  components: {
    zhuzhuangtu,
    zhexiantu
  }
}
</script>

<style>
#app {
  width: 100vw;
  height: 100vh;
background: rgb(109, 225, 109);
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding: 5px;
  /* margin-top: 60px; */
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  align-items: flex-start;
  align-content: flex-start;
}
.echarts-wraper{
  margin: 10px;
}
</style>
