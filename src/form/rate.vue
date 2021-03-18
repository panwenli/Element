<template>
  <div id="app">
    <div>
      <div class="block">
        <span class="demonstration">默认不区分颜色</span>
        <el-rate v-model="value1"></el-rate>
      </div>
      <div class="block">
        <span class="demonstration">区分颜色</span>
        <el-rate v-model="value2" :colors="colors"> </el-rate>
      </div>
    </div>
    <el-divider></el-divider>
    <div>
      <el-rate v-model="value" show-text> </el-rate>
    </div>
    <el-divider></el-divider>
    <div>
      <el-rate
        v-model="value3"
        :icon-classes="iconClasses"
        void-icon-class="icon-rate-face-off"
        :colors="['#99A9BF', '#F7BA2A', '#FF9900']"
      >
      </el-rate>
    </div>
    <el-divider></el-divider>
    <div>
      <el-rate
        v-model="value4"
        disabled
        show-score
        text-color="#ff9900"
        score-template="{value}"
      >
      </el-rate>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      value1: null,
      value2: null,
      colors: ["#99A9BF", "#F7BA2A", "#FF9900"],
      value: null,
      value3: null,
      iconClasses: ["icon-rate-face-1", "icon-rate-face-2", "icon-rate-face-3"],
      value4: 3.7
    };
  },
};
</script>

<style>
</style>