<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">

    <br>
    <input type="text" v-model="inputData"/>
    <button @click="onAddTextToList">Submit Text</button>
    <br>
    <p>{{ inputData }}</p>

    <ul>
      <li v-for="text in inputDataArr" :key="text">{{ text }}</li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'App',

  /*HERE I CAN DEFINE MY GLOBAL VARIABLES WITH THERE INITIALIZATION*/
  data() {
    return {
      inputData: null,
      inputDataArr: []
    }
  },

  /**THIS IS AN OPTION FOR THE FUNCTIONS */
  methods:{

    /**THIS METHOD ADD INPUTDATA TO MY ARR */
    onAddTextToList() {
      this.inputDataArr.push(this.inputData)
    }
  },
  components: {
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
</style>
