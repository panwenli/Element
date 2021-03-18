<template>
  <div id="app">
    <div>
      <div class="block">
        <span class="demonstration">有默认值</span>
        <el-color-picker v-model="color1"></el-color-picker>
      </div>
      <div class="block">
        <span class="demonstration">无默认值</span>
        <el-color-picker v-model="color2"></el-color-picker>
      </div>
    </div>
    <el-divider></el-divider>
    <div>
      <el-color-picker v-model="color" show-alpha></el-color-picker>
    </div>
    <el-divider></el-divider>
    <div>
      <el-color-picker v-model="color3" show-alpha :predefine="predefineColors">
      </el-color-picker>
    </div>
    <el-divider></el-divider>
    <div>
      <el-color-picker v-model="color4"></el-color-picker>
      <el-color-picker v-model="color4" size="medium"></el-color-picker>
      <el-color-picker v-model="color4" size="small"></el-color-picker>
      <el-color-picker v-model="color4" size="mini"></el-color-picker>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      color1: "#409EFF",
      color2: null,
      color: "rgba(19, 206, 102, 0.8)",
      color3: "rgba(255, 69, 0, 0.68)",
      color4: '#409EFF',
      predefineColors: [
        "#ff4500",
        "#ff8c00",
        "#ffd700",
        "#90ee90",
        "#00ced1",
        "#1e90ff",
        "#c71585",
        "rgba(255, 69, 0, 0.68)",
        "rgb(255, 120, 0)",
        "hsv(51, 100, 98)",
        "hsva(120, 40, 94, 0.5)",
        "hsl(181, 100%, 37%)",
        "hsla(209, 100%, 56%, 0.73)",
        "#c7158577",
      ],
    };
  },
};
</script>

<style>
</style>