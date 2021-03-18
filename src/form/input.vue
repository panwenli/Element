<template>
  <div id="app">
    <div>
      <el-input v-model="input" placeholder="请输入内容"></el-input>
    </div>
    <el-divider></el-divider>
    <div>
      <el-input
        placeholder="请输入内容"
        v-model="input1"
        :disabled="true"
      ></el-input>
    </div>
    <el-divider></el-divider>
    <div>
      <el-input placeholder="请输入内容" v-model="input2" clearable> </el-input>
    </div>
    <el-divider></el-divider>
    <div>
      <el-input
        placeholder="请输入密码"
        v-model="input3"
        show-password
      ></el-input>
    </div>
    <el-divider></el-divider>
    <div>
      <div class="demo-input-suffix">
        属性方式:
        <el-input
          placeholder="请输入日期"
          suffix-icon="el-icon-data"
          v-model="input4"
        ></el-input>
        <el-input
          placeholder="请输入内容"
          prefix-icon="el-cion-search"
          v-model="input5"
        ></el-input>
      </div>
      <div class="demo-input-suffix">
        solt 方式:
        <el-input placeholder="请选择日期" v-model="input6">
          <i slot="suffix" class="el-input_icon el-icon-date"></i>
        </el-input>
        <el-input placeholder="请输入内容" v-model="input7">
            <i slot="prefix" class="el-input_icon el-icon-search"></i>
        </el-input>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      input: "",
      input1: "",
      input2: "",
      input3: "",
      input4: "",
      input5: "",
      input6: "",
      input7: "",
    };
  },
};
</script>

<style>
</style>