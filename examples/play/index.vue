<template>
  <div>
    <div style="margin: 20px;">
      <el-input v-model="input" placeholder="请输入内容"></el-input>
    </div>
    <div style="margin: 20px;">
      <span>show-tag-max-number</span>
      <el-select
        v-model="value1"
        multiple
        collapse-tags
        :show-tag-max-number="2"
        placeholder="请选择"
        :style="{width: '200px'}"
      >
        <el-option
          v-for="item in options"
          :key="item.value"
          :label="item.label"
          :value="item.value">
        </el-option>
      </el-select>
    </div>
    <div style="margin: 20px;">
      <span>show-tag-max-number & 搜索</span>
      <el-select
        v-model="value2"
        multiple
        collapse-tags
        :show-tag-max-number="2"
        filterable
        placeholder="请选择"
        :style="{width: '200px'}"
      >
        <el-option
          v-for="item in options"
          :key="item.value"
          :label="item.label"
          :value="item.value">
        </el-option>
      </el-select>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        input: 'Hello Element UI!',
        options: [{
          value: '选项1',
          label: '黄金糕'
        }, {
          value: '选项2',
          label: '双皮奶'
        }, {
          value: '选项3',
          label: '蚵仔煎'
        }, {
          value: '选项4',
          label: '龙须面'
        }, {
          value: '选项5',
          label: '北京烤鸭'
        }],
        value1: ['选项1', '选项2', '选项3'],
        value2: ['选项1', '选项2', '选项3'],
      };
    }
  };
</script>
