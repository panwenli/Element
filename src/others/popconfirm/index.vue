<template>
  <div>
    <div>
      <el-popconfirm title="这是一段内容确定删除吗？">
        <el-button slot="reference">删除</el-button>
      </el-popconfirm>
    </div>
    <div>
      <el-popconfirm
        confirm-button-text="好的"
        cancel-button-text="不用了"
        icon="el-icon-info"
        icon-color="red"
        title="这是一段内容确定删除吗？"
      >
        <el-button slot="reference">删除</el-button>
      </el-popconfirm>
    </div>
  </div>
</template>

<style>
</style>

<script>
export default {};
</script>