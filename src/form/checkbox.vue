<template>
  <div id="app">
    <div>
      <el-checkbox v-model="checked">备选项</el-checkbox>
    </div>
    <el-divider></el-divider>
    <div>
      <el-checkbox v-model="checked1" disabled>备选项1</el-checkbox>
      <el-checkbox v-model="checked2" disabled>备选项</el-checkbox>
    </div>
    <el-divider></el-divider>
    <div>
      <el-checkbox-group v-model="checkList">
        <el-checkbox label="复选框 A"></el-checkbox>
        <el-checkbox label="复选框 B"></el-checkbox>
        <el-checkbox label="复选框 C"></el-checkbox>
        <el-checkbox label="禁用" disabled></el-checkbox>
        <el-checkbox label="选中且禁用" disabled></el-checkbox>
      </el-checkbox-group>
    </div>
    <el-divider></el-divider>
    <div>
      <el-checkbox
        :indeterminate="isIndeterminate"
        v-model="checkAll"
        @change="handleCheckAllChange"
        >全选</el-checkbox
      >
      <div style="margin: 15px 0"></div>
      <el-checkbox-group
        v-model="checkedCities"
        @change="handleCheckedCitiesChange"
      >
        <el-checkbox v-for="city in cities" :label="city" :key="city">{{
          city
        }}</el-checkbox>
      </el-checkbox-group>
    </div>
    <el-divider></el-divider>
    <div>
      <el-checkbox-group v-model="checkedCities1" :min="1" :max="2">
        <el-checkbox v-for="city in cities1" :label="city" :key="city">{{
          city
        }}</el-checkbox>
      </el-checkbox-group>
    </div>
    <el-divider></el-divider>
    <div>
      <div>
        <el-checkbox-group v-model="checkboxGroup1">
          <el-checkbox-button
            v-for="city in cities"
            :label="city"
            :key="city"
            >{{ city }}</el-checkbox-button
          >
        </el-checkbox-group>
      </div>
      <div style="margin-top: 20px">
        <el-checkbox-group v-model="checkboxGroup2" size="medium">
          <el-checkbox-button
            v-for="city in cities"
            :label="city"
            :key="city"
            >{{ city }}</el-checkbox-button
          >
        </el-checkbox-group>
      </div>
      <div style="margin-top: 20px">
        <el-checkbox-group v-model="checkboxGroup3" size="small">
          <el-checkbox-button
            v-for="city in cities"
            :label="city"
            :disabled="city === '北京'"
            :key="city"
            >{{ city }}</el-checkbox-button
          >
        </el-checkbox-group>
      </div>
      <div style="margin-top: 20px">
        <el-checkbox-group v-model="checkboxGroup4" size="mini" disabled>
          <el-checkbox-button
            v-for="city in cities2"
            :label="city"
            :key="city"
            >{{ city }}</el-checkbox-button
          >
        </el-checkbox-group>
      </div>
    </div>
    <el-divider></el-divider>
    <div>
      <div>
        <el-checkbox v-model="checked3" label="备选项1" border></el-checkbox>
        <el-checkbox v-model="checked4" label="备选项2" border></el-checkbox>
      </div>
      <div style="margin-top: 20px">
        <el-checkbox
          v-model="checked5"
          label="备选项1"
          border
          size="medium"
        ></el-checkbox>
        <el-checkbox
          v-model="checked6"
          label="备选项2"
          border
          size="medium"
        ></el-checkbox>
      </div>
      <div style="margin-top: 20px">
        <el-checkbox-group v-model="checkboxGroup5" size="small">
          <el-checkbox label="备选项1" border></el-checkbox>
          <el-checkbox label="备选项2" border disabled></el-checkbox>
        </el-checkbox-group>
      </div>
      <div style="margin-top: 20px">
        <el-checkbox-group v-model="checkboxGroup6" size="mini" disabled>
          <el-checkbox label="备选项1" border></el-checkbox>
          <el-checkbox label="备选项2" border></el-checkbox>
        </el-checkbox-group>
      </div>
    </div>
  </div>
</template>

<script>
const cityOptions = ["上海", "北京", "广州", "深圳"];
const cityOptions1 = ["上海", "北京", "广州", "深圳"];
const cityOptions2 = ["上海", "北京", "广州", "深圳"];
export default {
  data() {
    return {
      checked: true,
      checked1: false,
      checked2: true,
      checkList: ["选中且禁用", "复选框 A"],
      checkAll: false,
      checkedCities: ["上海", "北京"],
      cities: cityOptions,
      isIndeterminate: true,
      checkedCities1: ["上海", "北京"],
      cities1: cityOptions1,
      checkboxGroup1: ["上海"],
      checkboxGroup2: ["上海"],
      checkboxGroup3: ["上海"],
      checkboxGroup4: ["上海"],
      cities2: cityOptions2,
      checked3: true,
      checked4: false,
      checked5: false,
      checked6: true,
      checkboxGroup5: [],
      checkboxGroup6: [],
    };
  },
  methods: {
    handleCheckAllChange(val) {
      this.checkedCities = val ? cityOptions : [];
      this.isIndeterminate = false;
    },
    handleCheckedCitiesChange(value) {
      let checkedCount = value.length;
      this.checkAll = checkedCount === this.cities.length;
      this.isIndeterminate =
        checkedCount > 0 && checkedCount < this.cities.length;
    },
  },
};
</script>

<style>
</style>