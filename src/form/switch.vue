<template>
  <div id="app">
    <div>
      <el-switch
        v-model="value"
        active-color="#13ce66"
        inactive-color="#ff4949"
      >
      </el-switch>
    </div>
    <el-divider></el-divider>
    <div>
      <el-switch
        v-model="value1"
        active-text="按月付费"
        inactive-text="按年付费"
      >
      </el-switch>
      <el-switch
        style="display: block"
        v-model="value2"
        active-color="#13ce66"
        inactive-color="#ff4949"
        active-text="按月付费"
        inactive-text="按年付费"
      >
      </el-switch>
    </div>
    <el-divider></el-divider>
    <div>
      <el-tooltip :content="'Switch value: ' + value">
        <el-switch
          v-model="value3"
          active-color="#13ce66"
          inactive-color="#ff4949"
          active-value="100"
          inactive-value="0"
        >
        </el-switch>
      </el-tooltip>
    </div>
    <el-divider></el-divider>
    <div>
      <el-switch v-model="value4" disabled> </el-switch>
      <el-switch v-model="value5" disabled> </el-switch>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      value: true,
      value1: true,
      value2: true,
      value3: "100",
      value4: true,
      value5: false,
    };
  },
};
</script>

<style>
</style>