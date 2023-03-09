<template>
  <div id="app">
    <input type="text" v-model="channel.name" />
    <div>{{ name }}</div>

    <button @click="isShow = !isShow">
      <span v-if="isShow">An</span>
      <span v-else>Hien</span>
    </button>
    <h1 v-bind:id="id" v-show="isShow" :class="{ dachon: selected }"> Hieu IT TV Show</h1>
    <button @click="selected = !selected">Click</button>
    <button v-on:click="channel.name = 'ABC'">Change name</button>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import MyMenuMain from './components/MyMenuMain.vue';


export default {
  data() {
    return {
      channel: {
        name: 'Lap trinh abc'
      },
      id: 'abc',
      isShow: true,
      selected: true
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

.dachon {
  color: red;
}
</style>
