<template>
  <div>
    <el-row
      class="layout"
      v-for="(o, index) in 2"
      :key="o"
      :offset="index > 0 ? 1 : 0"
    >
      <el-col
        :span="8"
        v-for="(o, index) in 4"
        :key="o"
        :offset="index > 0 ? 1 : 0"
        class="setting"
      >
        <el-card :body-style="{ padding: '0px' }">
          <img src="../assets/tx.jpg" class="image" />
          <div style="padding: 14px">
            <span>好吃的汉堡</span>
            <div class="bottom clearfix">
              <time class="time">{{ currentDate }}</time>
            </div>
          </div>
        </el-card>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: "firstAid",
  data() {
    return {
      currentDate: new Date(),
    };
  },
};
</script>

<style scoped>
.layout {
  display: flex;
  justify-content: flex-start;
  margin-bottom: 180px;
}
.layout:nth-child(1) {
  margin-top: 20px;
}
.setting {
  width: 280px;
  height: 200px;
}
.time {
  font-size: 13px;
  color: #999;
}

.bottom {
  margin-top: 13px;
  line-height: 12px;
}

.button {
  padding: 0;
  float: right;
}

.image {
  width: 100%;
  display: block;
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: "";
}

.clearfix:after {
  clear: both;
}
/* img {
  width: 50px;
  height: 200px;
} */
</style>