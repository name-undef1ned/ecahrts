<template>
  <div class="echarts-wraper">
      <div id="zhexiantu">
      </div>
  </div>
</template>

<script>
export default {
name:'zhexiantu',
mounted() {
  // 1通过echartsd的init构造函数实例化echarts对象 传入dom节点（需要指定宽高）
    let myChart = this.$echarts.init(document.getElementById('zhexiantu'),'dark');
  // 通过实例的setOption方法配置图表
myChart.setOption({
  // 通过title对象字段指定标题
 title: {
          text: '折线图'
        },
          yAxis: {},

            xAxis: {
              type: 'category',
              data: ['Matcha Latte', 'Milk Tea', 'Cheese Cocoa', 'Walnut Brownie']
            },
series: [
    {
      type: 'line',
      name: '2015',
      data: [89.3, 92.1, 94.4, 85.4]
    },
    {
      type: 'line',
      name: '2016',
      data: [95.8, 89.4, 91.2, 76.9]
    },
    {
      type: 'line',
      name: '2017',
      data: [97.7, 83.1, 92.5, 78.1,],
      lineStyle:{
            normal: {
          color: 'green',
          width: 4,
          type: 'dashed'
        }
      },
        label: {
        show: true,
        position: 'bottom',
        textStyle: {
          fontSize: 20
        }
      },
       smooth: true
      
      
     
      
    }
  ]

})
},

}
</script>

<style>
#zhexiantu{
    width: 600px;
    height: 300px;
}
</style>