<template>
  <!--<input type="text" v-model="name" />--><!--to bind data property to the input we use v-model-->
  <Input v-model="name" /><!--we use v-model, to customize input component to bind name property-->
</template>

<script>
import Input from './components/custome-v-model.vue'
export default {
  name: 'App',
  components: {
    Input           // added list of component
  },
  data(){           // here first empty data object
    return{
      name: ''     // then add, define data property called name initialized with empty string
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
