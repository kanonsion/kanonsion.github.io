<template>
  <div :class="partSeven">
    <h3 class="text-center">求职意向</h3>
    <p class="text-small"><span class="font-bold">期望职位：</span>web前端实习</p>
    <p class="text-small"><span class="font-bold">工作技能：</span>Vue、js</p>
    <p class="text-small"><span class="font-bold">目标城市：</span>成都</p>
    <p class="text-small"><span class="font-bold">期望薪资：</span>2k-4k</p>
    <p class="text-small"><span class="font-bold">入职时间：</span>随时入职</p>
  </div>
</template>

<script>
export default {
  name: "partSeven",
  data() {
    return {
      partSeven: "part-seven",
      curWidth: 0
    };
  },
  beforeMount() {
    this.curWidth = document.documentElement.clientWidth || document.body.clientWidth;
    if(this.curWidth < 1600) {
      this.partSeven = "part-sevev-responsive"
    }
  }
};
</script>

<style scoped>
.part-seven {
  width: 100%;
  height: 310px;
  border: 40px solid transparent;
  border-image: url("~@/./assets/img/border_image.png") 30 30 stretch;
  background: #18202d;
}
.part-sevev-responsive {
  width: 100%;
  border: 40px solid transparent;
  border-image: url("~@/./assets/img/border_image.png") 30 30 stretch;
  background: #18202d; 
}
.text-center {
  text-align: center;
}
.text-small {
  font-size: .9em;
}
.font-bold {
  text-align: center;
  color: deepskyblue;
}
</style>