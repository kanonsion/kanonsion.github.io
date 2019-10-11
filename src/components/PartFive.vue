<template>
  <div :class="partFive" class="scrool">
    <h3 class="text-center text-top">项目经验</h3>
    <div>
      <p>
        <a href="javascript:void(0)">zd后台管理系统</a>
        <span class="text-small">| 2019/8-2019/9</span>
      </p>
      <p class="text-small">主要技术：vue 、 vue-router 、axios 、 elementUI 、 jwt验证</p>
      <p class="text-small">项目描述：</p>
      <p class="text-small">&emsp;1. 使用vue-cli 3.0搭建的vue项目</p>
      <p class="text-small">&emsp;2. 主要负责接口对接，前台页面展示，登录之后的后台管理系统，能够进行增删查改等基本操作，以及简单的权限控制，文件上传下载</p>
      <p class="text-small">&emsp;3. 利用axios的全局响应请求拦截，通过token对用户登录做判断</p>
    </div>
    <p></p>
    <div>
      <p>
        <a href="javascript:void(0)">内江师范科研系统</a>
        <span class="text-small">| 2019/3 – 2019/5</span>
      </p>
      <p class="text-small">主要技术:  vue 、 layui 、 jQuery 、 SVN</p>
      <p class="text-small">项目描述：</p>
      <p class="text-small">&emsp;主要负责对艺术作品这个模块的数据渲染，合法判断，增加，删除，查找等操作</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "partFive",
  data() {
    return {
      partFive: "part-five",
      curWidth: 0
    };
  },
  beforeMount() {
    this.curWidth =
      document.documentElement.clientWidth || document.body.clientWidth;
    if (this.curWidth < 1600) {
      this.partFive = "part-five-responsive";
    }
  }
};
</script>

<style scoped>
a {
  color: deepskyblue;
}
a:hover {
  color: rgb(118, 190, 248);
}
.part-five {
  width: 100%;
  height: 310px;
  border: 40px solid transparent;
  border-image: url("~@/./assets/img/border_image.png") 30 30 stretch;
  background: #18202d;
}
.part-five-responsive {
  width: 100%;
  border: 40px solid transparent;
  border-image: url("~@/./assets/img/border_image.png") 30 30 stretch;
  background: #18202d;
  height: 310px;
  overflow-y: scroll;
}
/*滚动条样式*/
.part-five::-webkit-scrollbar {
  /*滚动条整体样式*/
  width: 4px; /*高宽分别对应横竖滚动条的尺寸*/
  height: 4px;
}
.part-five::-webkit-scrollbar-thumb {
  /*滚动条里面小方块*/
  border-radius: 5px;
  -webkit-box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.2);
  background: rgba(0, 0, 0, 0.3);
}
.part-five::-webkit-scrollbar-track {
  /*滚动条里面轨道*/
  -webkit-box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.2);
  border-radius: 0;
  background: rgba(0, 0, 0, 0.1);
}
/*滚动条样式*/
.part-five-responsive::-webkit-scrollbar {
  /*滚动条整体样式*/
  width: 4px; /*高宽分别对应横竖滚动条的尺寸*/
  height: 4px;
}
.part-five-responsive::-webkit-scrollbar-thumb {
  /*滚动条里面小方块*/
  border-radius: 5px;
  -webkit-box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.2);
  background: rgba(0, 0, 0, 0.3);
}
.part-five-responsive::-webkit-scrollbar-track {
  /*滚动条里面轨道*/
  -webkit-box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.2);
  border-radius: 0;
  background: rgba(0, 0, 0, 0.1);
}
.text-center {
  text-align: center;
}
.text-small {
  font-size: 0.9em;
  color: rgb(253, 239, 239);
}
</style>