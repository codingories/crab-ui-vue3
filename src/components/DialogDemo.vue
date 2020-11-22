<template>
  <h1>Dialog 示例</h1>
  <Demo :component="Dialog1Demo" />
  <Demo :component="Dialog2Demo" />
  <attr :columns="columns" :data="data"></attr>
</template>

<script lang="ts">
  import Demo from './Demo.vue';
  import Dialog1Demo from './Dialog1.demo.vue';
  import Dialog2Demo from './Dialog2.demo.vue';
  import Attr from './Attr.vue'
  import {columns} from "../lib/data";

  export default {
    components: {
      Demo,Attr
    },

    setup() {
      const data = [
        {
          params: 'visible',
          desc: '是否展示',
          type: 'boolean',
          select: 'true / false',
          default: 'normal',
        },
        {
          params: 'ok',
          desc: '确认触发函数',
          type: 'function',
          select: '()=>{}',
          default: '--',
        },
        {
          params: 'cancel',
          desc: '取消触发函数',
          type: 'function',
          select: '()=>{}',
          default: '--',
        },
      ];
      return {
        Dialog1Demo,
        Dialog2Demo,
        columns,
        data,
      }
    }
  }
</script>
