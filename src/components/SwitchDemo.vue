<template>
  <div>
    <h1>Switch 组件示例 </h1>
    <Demo :component="Switch1Demo" />
    <Demo :component="Switch2Demo" />
    <attr :columns="columns" :data="data"></attr>

  </div>
</template>

<script lang="ts">
  import Switch1Demo from './Switch1.demo.vue'
  import Switch2Demo from './Switch2.demo.vue'
  import Attr from './Attr.vue'
  import Demo from './Demo.vue'
  import {columns} from "../lib/data";

  // const Prism = (window as any).Prism;
  // console.log('fuck0',window.Prism);
  export default {
    components: {
      Demo, Attr
    },
    setup() {
      const data = [
        {
          params: 'value',
          desc: '是否选中',
          type: 'boolean',
          select: 'false / true',
          default: 'false',
        }
      ];
      return {
        Switch1Demo,Switch2Demo,data,columns
      }
    }
  }
</script>

<style lang="scss" scoped>
</style>
