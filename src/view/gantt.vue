<template>
  <div class="wrap" ref="gantt">
    <h1>common!</h1>
  </div>
</template>

<script>
import 'dhtmlx-gantt'

export default {
  name: 'gantt',
  props: {
    tasks: {
      type: Object,
      default () {
        return {data: [], links: []}
      }
    }
  },
  data() {
    return {

    }
  },
  mounted() {
    gantt.init(this.$refs.gantt)
    gantt.parse(this.$props.tasks)
  }
}
</script>

<style>
  @import "~dhtmlx-gantt/codebase/dhtmlxgantt.css";

  .wrap {
    height: 100%;
  }
</style>