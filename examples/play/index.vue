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
    <div style="margin: 20px;">
      <span>cascader show-tag-max-number</span>
      <el-cascader
        v-model="value3"
        :options="options2"
        :props="{multiple: true}"
        collapse-tags
        clearable
        :show-tag-max-number="3"
      >
      </el-cascader>
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
        options2: [{
          value: 1,
          label: '东南',
          children: [{
            value: 2,
            label: '上海',
            children: [
              { value: 3, label: '普陀' },
              { value: 4, label: '黄埔' },
              { value: 5, label: '徐汇' }
            ]
          }, {
            value: 7,
            label: '江苏',
            children: [
              { value: 8, label: '南京' },
              { value: 9, label: '苏州' },
              { value: 10, label: '无锡' }
            ]
          }, {
            value: 12,
            label: '浙江',
            children: [
              { value: 13, label: '杭州' },
              { value: 14, label: '宁波' },
              { value: 15, label: '嘉兴' }
            ]
          }]
        }, {
          value: 17,
          label: '西北',
          children: [{
            value: 18,
            label: '陕西',
            children: [
              { value: 19, label: '西安' },
              { value: 20, label: '延安' }
            ]
          }, {
            value: 21,
            label: '新疆维吾尔族自治区',
            children: [
              { value: 22, label: '乌鲁木齐' },
              { value: 23, label: '克拉玛依' }
            ]
          }]
        }],
        value1: ['选项1', '选项2', '选项3'],
        value2: ['选项1', '选项2', '选项3'],
        value3: [[1,2,4], [1,2,5],[1,7,8],[17,18,20]],
      };
    }
  };
</script>
