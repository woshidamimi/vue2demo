
<template>
  <div class="arc-chart" ref="arcChart"></div>
</template>
<script>
import * as Echarts from 'echarts'
export default {
  name: "ArcChart",
  components: {},
  data() {
    return {};
  },
  computed: {},
  watch: {},
  created() {},
  mounted() {
      this.init();
  },
  methods: {
      init() {
          const dom = this.$refs.arcChart;
          if(!dom) {
              return false;
          }
          console.log(Echarts)
          const instance = Echarts.init(dom);
          console.log(instance)

          let option = {
              graphic: [
                  {
                      type: 'arc',
                      shape: {
                          cx: 250,
                          cy: 250,
                          r: 130,
                        //   r0: 10,
                          startAngle: 0,
                          endAngle: Math.PI * 1,
                          clockwise: false
                      },
                      style: {
                        //   fill: 'red',
                          stroke: '#41b883',
                          lineWidth: 50
                      }
                  },
                  {
                      type: 'polygon',
                      shape: {
                          points: [[110,280], [230, 450], [350, 280]]
                      },
                      style: {
                          fill: '#41b883'
                      }
                  },
                  {
                      type: 'polygon',
                      shape: {
                          points: [[150,280], [230, 400], [310, 280]]
                      },
                      style: {
                          fill: '#35495e'
                      }
                  }
              ]
          }

          instance.setOption(option)
      }
  }
};
</script>
<style lang="css" scoped>
.arc-chart {
  width: 500px;
  height: 500px;
  background: #fafafa;
  margin: 0 auto;
}
</style>