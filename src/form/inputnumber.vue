<template>
  <div>
    <div>
      <el-input-number
        v-model="num"
        @change="handleChange"
        :min="1"
        :max="10"
        label="描述文字"
      ></el-input-number>
    </div>
    <el-divider></el-divider>
    <div>
      <el-input-number v-model="num1" :disabled="true"></el-input-number>
    </div>
    <el-divider></el-divider>
    <div>
      <el-input-number v-model="num2" :step="2"></el-input-number>
    </div>
    <el-divider></el-divider>
    <div>
      <el-input-number v-model="num3" :step="2" step-strictly></el-input-number>
    </div>
    <el-divider></el-divider>
    <div>
      <el-input-number
        v-model="num4"
        :precision="2"
        :step="0.1"
        :max="10"
      ></el-input-number>
    </div>
    <el-divider></el-divider>
    <div>
      <el-input-number v-model="num5"></el-input-number>
      <el-input-number size="medium" v-model="num6"></el-input-number>
      <el-input-number size="small" v-model="num7"></el-input-number>
      <el-input-number size="mini" v-model="num8"></el-input-number>
    </div>
    <el-divider></el-divider>
    <div>
      <el-input-number
        v-model="num9"
        controls-position="right"
        @change="handleChange1"
        :min="1"
        :max="10"
      ></el-input-number>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num: 1,
      num1: 1,
      num2: 5,
      num3: 2,
      num4: 1,
      num5: 1,
      num6: 1,
      num7: 1,
      num8: 1,
      num9: 1,
    };
  },
  methods: {
    handleChange(value) {
      console.log(value);
    },
    handleChange1(value) {
      console.log(value);
    },
  },
};
</script>

<style>
</style>