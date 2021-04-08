<template>
  <div id="app">
    <div>
      <el-button plain @click="open1"> 可自动关闭 </el-button>
      <el-button plain @click="open2"> 不会自动关闭 </el-button>
    </div>
    <el-divider></el-divider>
    <div>
      <el-button plain @click="open1A"> 成功 </el-button>
      <el-button plain @click="open2B"> 警告 </el-button>
      <el-button plain @click="open3C"> 消息 </el-button>
      <el-button plain @click="open4D"> 错误 </el-button>
    </div>
    <el-divider></el-divider>
    <div>
      <el-button plain @click="open1S"> 右上角 </el-button>
      <el-button plain @click="open2SS"> 右下角 </el-button>
      <el-button plain @click="open3SSS"> 左下角 </el-button>
      <el-button plain @click="open4SSR"> 左上角 </el-button>
    </div>
    <el-divider></el-divider>
    <div>
      <el-button plain @click="open"> 偏移的消息 </el-button>
    </div>
    <el-divider></el-divider>
    <div>
      <el-button plain @click="openA"> 使用 HTML 片段 </el-button>
    </div>
    <el-divider></el-divider>
    <div>
      <el-button plain @click="openB"> 隐藏关闭按钮 </el-button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    open1() {
      const h = this.$createElement;

      this.$notify({
        title: "标题名称",
        message: h("i", { style: "color: teal" }, "这是提示文案"),
      });
    },
    open2() {
      this.$notify({
        title: "提示",
        message: "这是一条不会自动关闭的消息",
        duration: 0,
      });
    },

    open1A() {
      this.$notify({
        title: "成功",
        message: "这是一条成功的提示消息",
        type: "success",
      });
    },
    open2B() {
      this.$notify({
        title: "警告",
        message: "这是一条警告的提示消息",
        type: "warning",
      });
    },
    open3C() {
      this.$notify.info({
        title: "消息",
        message: "这是一条消息的提示消息",
      });
    },
    open4D() {
      this.$notify.error({
        title: "错误",
        message: "这是一条错误的提示消息",
      });
    },

    open1S() {
      this.$notify({
        title: "自定义位置",
        message: "右上角弹出的消息",
      });
    },
    open2SS() {
      this.$notify({
        title: "自定义位置",
        message: "右下角弹出的消息",
        position: "bottom-right",
      });
    },
    open3SSS() {
      this.$notify({
        title: "自定义位置",
        message: "左下角弹出的消息",
        position: "bottom-left",
      });
    },
    open4SSR() {
      this.$notify({
        title: "自定义位置",
        message: "左上角弹出的消息",
        position: "top-left",
      });
    },

    open() {
      this.$notify({
        title: "偏移",
        message: "这是一条带有偏移的提示消息",
        offset: 100,
      });
    },

    openA() {
      this.$notify({
        title: "HTML 片段",
        dangerouslyUseHTMLString: true,
        message: "<strong>这是 <i>HTML</i> 片段</strong>",
      });
    },

    openB() {
        this.$notify.success({
          title: 'Info',
          message: '这是一条没有关闭按钮的消息',
          showClose: false
        });
      }
  },
};
</script>

<style>
</style> 