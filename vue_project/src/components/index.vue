<template>
  <div>
    <el-carousel indicator-position="outside" class="top">
      <el-carousel-item v-for="item in 4" :key="item">
        <h3>{{ item }}</h3>
      </el-carousel-item>
    </el-carousel>
    <div class="tip" v-show="isShow">
      <div>暖心小tips</div>
      <div>
        不管你正在经历什么，都请相信，一切都会好起来的，生活有时候难免会有坎坷，但是我们总是能够走出来的
      </div>
      <div @click="isShow = false"><img src="../assets/close.png" /></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "indexView",
  data() {
    return {
      isShow: true,
    };
  },
  mounted() {
    this.show();
  },
  methods: {
    show() {
      clearInterval(this.timer);
      this.timer = setInterval(() => {
        this.isShow = false;
      }, 5000);
    },
  },
};
</script>

<style>
.el-carousel__item h3 {
  color: #475669;
  font-size: 18px;
  opacity: 0.75;
  line-height: 300px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}
.top {
  margin-top: 10px;
}
.tip {
  position: absolute;
  width: 400px;
  height: 200px;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  background-color: #fff;
  z-index: 9;
  border-radius: 10px;
}
.tip div:nth-child(1) {
  padding-top: 35px;
}
.tip div:nth-child(2) {
  width: 280px;
  overflow: auto;
  text-align: center;
  margin: 40px auto;
}
.tip div:last-child {
  position: absolute;
  z-index: 10;
  top: 15px;
  right: 15px;
  width: 20px;
  height: 20px;
  overflow: hidden;
}
.tip div img {
  width: 100%;
  height: 100%;
}
</style>