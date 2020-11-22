<template>
  <h1>Tabs 示例</h1>
  <Demo :component="Tabs1Demo" />
  <attr :columns="columns" :data="data"></attr>
</template>

<script lang="ts">
  import Demo from './Demo.vue'
  import Tabs1Demo from './Tabs1.demo.vue'
  import Attr from './Attr.vue'
  import {columns} from "../lib/data";

  export default {
    components: {
      Demo,Attr
    },
    setup() {
      const data = [
        {
          params: 'Tab',
          desc: 'tab页签',
          type: 'component',
          select: 'Tab',
          default: '--',
        },
      ];
      return {
        Tabs1Demo,
        columns,
        data
      }
    }
  }
</script>
