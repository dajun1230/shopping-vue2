<template>
  <div class="user">
    <div>当前数量：{{ count }}</div>
    <el-button type="primary" @click="addCount">新增</el-button>
    <el-button type="success" @click="reduceCount">减少</el-button>
    <!-- <router-link to='home'>首页</router-link>
      <router-link to='about'>关于</router-link> -->
    <div class="block">
      <span class="demonstration">当前日期：</span>
      <el-date-picker v-model="date" type="date" placeholder="选择日期">
      </el-date-picker>
    </div>
  </div>
</template>

<script>
export default {
  name: "home",
  data() {
    return {
      name: "哈哈哈",
      count: 0,
      date: new Date(),
    };
  },
  mounted() {
    // console.log("mounted:", this);
  },
  methods: {
    addCount() {
      this.count++;
    },
    reduceCount: function () {
      this.count--;
    },
  },
};
</script>

<style scoped>
.user {
  border: 1px solid red;
}
</style>
