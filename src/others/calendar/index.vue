<script src="//unpkg.com/vue/dist/vue.js"></script>
<script src="//unpkg.com/element-ui@2.15.1/lib/index.js"></script>

<template>
  <div>
    <div>
      <el-calendar v-model="value"> </el-calendar>
    </div>
    <div>
      <el-calendar>
        <template slot="dateCell" slot-scope="{ date, data }">
          <p :class="data.isSelected ? 'is-selected' : ''">
            {{ data.day.split("-").slice(1).join("-") }}
            {{ data.isSelected ? "✔️" : "" }}
          </p>
        </template>
      </el-calendar>
    </div>
    <div>
      <el-calendar :range="['2019-03-04', '2019-03-24']"> </el-calendar>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      value: new Date(),
    };
  },
};
</script>

<style>
.is-selected {
  color: #1989fa;
}
</style>