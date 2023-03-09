<template>
  <div id="app">
    <input type="text" v-model="NewTask">
    <button @click="addTask()">Them tasks</button>
    <div v-for="(task, index) in tasks" :key="index">
      <input type="checkbox" v-model="task.done">
      <span :class="{ done: task.done }">{{ task.content }}</span>
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import MyMenuMain from './components/MyMenuMain.vue';


export default {
  data() {
    return {
      NewTask: '',
      tasks: []
    }
  },
  methods: {
    addTask: function () {
      this.tasks.push({ content: this.NewTask, done: false })
    }
  },
  mounted() {
    //goi api
  },
  watch: {
    NewTask: function (newValue, oldValue) {
      console.log(oldValue);
      console.log(newValue)
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.done {
  text-decoration: line-through;
}

.dachon {
  color: red;
}
</style>
