<template>
  <div>
    <h1>Button 示例</h1>
    <Demo :component="Button1Demo" />
    <Demo :component="Button2Demo" />
    <Demo :component="Button3Demo" />
    <Demo :component="Button4Demo" />
    <Demo :component="Button5Demo" />
    <attr :columns="columns" :data="data"></attr>
  </div>
</template>

<script lang="ts">
  import Demo from "./Demo.vue";
  import Button1Demo from "./Button1.demo.vue";
  import Button2Demo from "./Button2.demo.vue";
  import Button3Demo from "./Button3.demo.vue";
  import Button4Demo from "./Button4.demo.vue";
  import Button5Demo from "./Button5.demo.vue";
  import Attr from './Attr.vue'
  import {columns} from "../lib/data";
  export default {

    components: {
      Attr,
      Demo
    },
    setup() {
      const data = [
        {
          params: 'size',
          desc: '尺寸',
          type: 'string',
          select: 'normal / small / mini',
          default: 'normal',
        },
        {
          params: 'theme',
          desc: '按钮类型',
          type: 'string',
          select: 'primary / success / warning / info / danger / text',
          default: 'primary',
        },
        {
          params: 'loading',
          desc: '加载中',
          type: 'boolean',
          select: 'false / true',
          default: 'false',
        }
      ]
      return {
        Button1Demo,
        Button2Demo,
        Button3Demo,
        Button4Demo,
        Button5Demo,
        columns,
        data
      };
    },
  };
</script>
