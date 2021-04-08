<template>
  <div id="app">
    <div>
      <el-page-header @back="goBack" content="详情页面"> </el-page-header>
    </div>
  </div>
</template>

<style>
</style>

<script>
export default {
  methods: {
    goBack() {
      console.log("go back");
    },
  },
};
</script>