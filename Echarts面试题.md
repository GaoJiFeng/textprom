# Echarts 可视化工具面试题

## 1、为什么要用数据可视化

数据可视化可以更直观更清晰的把数据展示出来，便于分析，解读

## 2、数据可视化分为哪几类

信息可视化、可视化分析、科学可视化

## 3、Echarts可视化工具可以做什么

ECharts 提供了常规的[折线图](https://echarts.apache.org/zh/option.html#series-line)、[柱状图](https://echarts.apache.org/zh/option.html#series-bar)、[散点图](https://echarts.apache.org/zh/option.html#series-scatter)、[饼图](https://echarts.apache.org/zh/option.html#series-pie)、[K线图](https://echarts.apache.org/zh/option.html#series-candlestick)，用于统计的[盒形图](https://echarts.apache.org/zh/option.html#series-boxplot)，用于地理数据可视化的[地图](https://echarts.apache.org/zh/option.html#series-map)、[热力图](https://echarts.apache.org/zh/option.html#series-heatmap)、[线图](https://echarts.apache.org/zh/option.html#series-lines)，用于关系数据可视化的[关系图](https://echarts.apache.org/zh/option.html#series-graph)、[treemap](https://echarts.apache.org/zh/option.html#series-treemap)、[旭日图](https://echarts.apache.org/zh/option.html#series-sunburst)，多维数据可视化的[平行坐标](https://echarts.apache.org/zh/option.html#series-parallel)，还有用于 BI 的[漏斗图](https://echarts.apache.org/zh/option.html#series-funnel)，[仪表盘](https://echarts.apache.org/zh/option.html#series-gauge)，并且支持图与图之间的混搭

## 4、如何安装Echarts

1）、npm安装 通过npm install echarts --save/cnpm install echarts --save

2)、从 [Apache ECharts (incubating) 官网下载界面](https://echarts.apache.org/download.html) 获取官方源码包后构建

## 5、vue项目中如何使用Echarts

1）、使用npm install echarts --save/cnpm install echarts --save创建echarts模块

2）、在main.js中引入

```javascript
import echarts from 'echarts'
Vue.prototype.$echarts = echarts
```

3）、在页面挂挂载生命周期函数中生成实例化

```javascript
mounted() {
    this.drawLine();
  },
  methods: {
    drawLine() {
     
      let myChart = this.$echarts.init(
        document.getElementsByClassName("home")[0]
      );
      
      myChart.setOption({
        legend: {
          orient: "vertical",
          right: 10,
          top: 200,
          data: ["考点专练", "套卷练习", "仿真模拟"]
        },
        graphic: {
          
          type: "text",
          left: "center",
          top: "center",
          backgroundColor:'black',
          style: {
            text: "0\n做题数",
            textAlign: "center",
            fill: "black",
            fontSize: 20,
            
          }
        },

        color: ["rgb(245,178,108)", "rgb(87,187,171)", "rgb(163, 233, 165)"],
        series: [
          {
            name: "访问来源",
            type: "pie",
            radius: [60, 120],
            avoidLabelOverlap: false,
            label: {
              show: false,
              position: "center"
            },
            emphasis: {
              label: {
                show: true,
                fontSize: "20",
                fontWeight: "bold"
              }
            },
            labelLine: {
              show: false
            },
            data: [
              { value: 30, name: "考点专练" },
              { value: 30, name: "套卷练习" },
              { value: 30, name: "仿真模拟" }
            ]
          }
        ]
      });
    }
  }
```

以上为饼状图的代码

