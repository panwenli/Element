<script src="//unpkg.com/vue/dist/vue.js"></script>
<script src="//unpkg.com/element-ui@2.15.1/lib/index.js"></script>

<template>
  <div id="app">
    <div>
      <div class="block">
        <span class="demonstration">页数较少时的效果</span>
        <el-pagination layout="prev, pager, next" :total="50"> </el-pagination>
      </div>
      <div class="block">
        <span class="demonstration">大于 7 页时的效果</span>
        <el-pagination layout="prev, pager, next" :total="1000">
        </el-pagination>
      </div>
    </div>
    <el-divider></el-divider>
    <div>
      <el-pagination
        :page-size="20"
        :pager-count="11"
        layout="prev, pager, next"
        :total="1000"
      >
      </el-pagination>
    </div>
    <el-divider></el-divider>
    <div>
      <el-pagination background layout="prev, pager, next" :total="1000">
      </el-pagination>
    </div>
    <el-divider></el-divider>
    <div>
      <el-pagination small layout="prev, pager, next" :total="50">
      </el-pagination>
    </div>
    <el-divider></el-divider>
    <div>
      <div class="block">
        <span class="demonstration">显示总数</span>
        <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page.sync="currentPage1"
          :page-size="100"
          layout="total, prev, pager, next"
          :total="1000"
        >
        </el-pagination>
      </div>
      <div class="block">
        <span class="demonstration">调整每页显示条数</span>
        <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page.sync="currentPage2"
          :page-sizes="[100, 200, 300, 400]"
          :page-size="100"
          layout="sizes, prev, pager, next"
          :total="1000"
        >
        </el-pagination>
      </div>
      <div class="block">
        <span class="demonstration">直接前往</span>
        <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page.sync="currentPage3"
          :page-size="100"
          layout="prev, pager, next, jumper"
          :total="1000"
        >
        </el-pagination>
      </div>
      <div class="block">
        <span class="demonstration">完整功能</span>
        <el-pagination
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
          :current-page="currentPage4"
          :page-sizes="[100, 200, 300, 400]"
          :page-size="100"
          layout="total, sizes, prev, pager, next, jumper"
          :total="400"
        >
        </el-pagination>
      </div>
    </div>
    <el-divider></el-divider>
    <div>
      <el-switch v-model="value"> </el-switch>
      <el-pagination
        :hide-on-single-page="value"
        :total="5"
        layout="prev, pager, next"
      >
      </el-pagination>
    </div>
  </div>
</template>

<style>
</style>

<script>
export default {
  methods: {
    handleSizeChange(val) {
      console.log(`每页 ${val} 条`);
    },
    handleCurrentChange(val) {
      console.log(`当前页: ${val}`);
    },
  },
  data() {
    return {
      currentPage1: 5,
      currentPage2: 5,
      currentPage3: 5,
      currentPage4: 4,
      value: false
    };
  },
};
</script>