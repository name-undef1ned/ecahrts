<template>
  <div class="echarts-wraper">
      <div id="zhuzhuangtu" >
      </div>
  </div>
</template>

<script>
export default {
name:'zhuzhuangtu',
mounted() {
  // 1通过echartsd的init构造函数实例化echarts对象 传入dom节点（需要指定宽高）
    let myChart = this.$echarts.init(document.getElementById('zhuzhuangtu'),'dark');
  // 通过实例的setOption方法配置图表
myChart.setOption({
  // 通过title对象字段指定标题
 title: {
          text: '柱状图'
        },
          yAxis: {},

            xAxis: {
              type: 'category',
              data: ['Matcha Latte', 'Milk Tea', 'Cheese Cocoa', 'Walnut Brownie']
            },
series: [
    {
      type: 'bar',
      name: '2015',
      data: [89.3, 92.1, 94.4, 85.4]
    },
    {
      type: 'bar',
      name: '2016',
      data: [95.8, 89.4, 91.2, 76.9],
      
    },
    {
      type: 'bar',
      name: '2017',
      data: [97.7, 83.1, 92.5, 78.1,],
       // 设置单个柱子的样式
          itemStyle: {
            color: '#91cc75',
            shadowColor: '#91cc75',
            borderType: 'dashed',
            opacity: 0.5
          },
          barWidth :'20%',
            showBackground: true,
          backgroundStyle: {
        color: 'white'
      },
        label: {
        show: true,
        position: 'center',
        textStyle: {
          fontSize: 10
        }
      }
      
    }
  ],
  legend:{
    type:'scroll'
  },
  tooltip:{
    show:true
  }

})
},

}
</script>

<style>
#zhuzhuangtu{
    width: 600px;
    height: 300px;
}
</style>