<!--what is customize v-model-- if 2 companies one is accentur another one is tcs they are want to input in differnt data and differnt style. then we will create a single customize-v-model-->
<template>
  <Input type="text" :value="modelValue" :maxlength="max" @input="$emit('update:modelValue', $event.target.value)"/>
  <!--if the given input is does't store the data property we will define some changes,
when we use v-model in custome component it automatically receive prop call(modelvalue), 
we need to specify in the props option. 
next we need to bind the props to the value attribute of input element (:value="modelValue", this will be take care of value of the input)
when we use v-model directive in custome component it automaticaly listen to an event called 'update:modelValue',
so the input element we bind to the input element and emit the update 'update:modelValue', then the data we passed to the parent is ($event.target.value)which is input element value-->
</template>
<script>
export default {
  name: 'customeV',
  props: {
    modelValue: String      // here specify the props 
  },
  data() {
    return{
      max: 16,
    }
  }
}
</script>
<style scoped>
  Input[type='text'] {
    display: block;
    text-align: center;
    margin-top: 60px;
    width: 250px;
    padding: 6px 12px;
    font-size: 14px;
    line-height: 1.4 ;
    color: rgb(255, 255, 255);
    background-color:rgb(4, 42, 118) ;
    border: 1px solid #ccc;
    border-radius: 4px;
    margin : 0 auto;
    
  }
</style>