<template>
  <div id="gaodeMap"></div>
</template>
<script>
import AMap from "AMap";
export default {
  data() {
    return {
      amap: {},
    };
  },
  mounted() {
    this.drawGaodeMap();
  },
  methods: {
    drawGaodeMap() {
      this.amap = new AMap.Map("gaodeMap", {
        resizeEnable: true,
        // zoom: 3, //级别
        layers: [new AMap.TileLayer.Satellite()],//Satellite()表示卫星图
        lang: "zh", //可选值：en，zh_en, zh_cn
        center: [120.587634, 30.040461],//中心点坐标
        zoom: 13,//级别,数字越大越精细
        //viewMode:'3D'//使用3D视图
      });
      var scale = new AMap.Scale(),
        toolBar = new AMap.ToolBar(),
        overView = new AMap.OverView();
      this.amap.addControl(scale);
      this.amap.addControl(toolBar);
      this.amap.addControl(overView);
    },
  },
};
</script>
<style>
#gaodeMap {
  width: 100vw;
  height: 100vh;
}
</style>