<template>
  <div id="app" class="container">
    <gantt class="left-container" :tasks="tasks"></gantt>
  </div>
</template>

<script>
import Gantt from "@/view/gantt"
export default {
  name: 'app',
  components: {
    Gantt
  },
  data () {
    return {
      tasks: {
        data: [
          {id: 1, text: 'Task #1', start_date: '15-04-2017', duration: 3, progress: 0.6},
          {id: 2, text: 'Task #2', start_date: '20-04-2017', duration: 6, progress: 0.4}
        ],
        links: [
          {id: 1, source: 1, target: 2, type: '0'}
        ]
      },
    }
  }
}
</script>

<style>
html, body {
  padding: 0;
  margin: 0;
  width: 100%;
  height: 100%;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
