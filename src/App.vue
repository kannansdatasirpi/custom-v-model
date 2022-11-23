<template>
  <!--<input type="text" v-model="name" />--><!--to bind data property to the input we use v-model-->
  <Input v-model="name" /><!--we use v-model, custome input component to bind name property-->
</template>

<script>
import Input from './components/custome-v-model.vue'
export default {
  name: 'App',
  components: {
    Input
  },
  data(){
    return{
      name: ''
    }
  },
  methods: {},
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
