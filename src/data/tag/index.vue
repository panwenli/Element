<template>
  <div id="app">
    <div>
      <el-tag>标签一</el-tag>
      <el-tag type="success">标签二</el-tag>
      <el-tag type="info">标签三</el-tag>
      <el-tag type="warning">标签四</el-tag>
      <el-tag type="danger">标签五</el-tag>
    </div>
    <el-divider></el-divider>
    <div>
      <el-tag v-for="tag in tags" :key="tag.name" closable :type="tag.type">
        {{ tag.name }}
      </el-tag>
    </div>
    <el-divider></el-divider>
    <div>
      <el-tag closable>默认标签</el-tag>
      <el-tag size="medium" closable>中等标签</el-tag>
      <el-tag size="small" closable>小型标签</el-tag>
      <el-tag size="mini" closable>超小标签</el-tag>
    </div>
    <el-divider></el-divider>
    <div>
      <div class="tag-group">
        <span class="tag-group__title">Dark</span>
        <el-tag
          v-for="item in items"
          :key="item.label"
          :type="item.type"
          effect="dark"
        >
          {{ item.label }}
        </el-tag>
      </div>
      <div class="tag-group">
        <span class="tag-group__title">Plain</span>
        <el-tag
          v-for="item in items"
          :key="item.label"
          :type="item.type"
          effect="plain"
        >
          {{ item.label }}
        </el-tag>
      </div>
    </div>
  </div>
</template>

<style>
</style>

<script>
export default {
  data() {
    return {
      tags: [
        { name: "标签一", type: "" },
        { name: "标签二", type: "success" },
        { name: "标签三", type: "info" },
        { name: "标签四", type: "warning" },
        { name: "标签五", type: "danger" },
      ],
      items: [
        { type: "", label: "标签一" },
        { type: "success", label: "标签二" },
        { type: "info", label: "标签三" },
        { type: "danger", label: "标签四" },
        { type: "warning", label: "标签五" },
      ],
    };
  },
};
</script>