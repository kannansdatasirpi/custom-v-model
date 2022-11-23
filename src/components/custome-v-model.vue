<template>
  <Input type="text" :value="modelValue" @input="$emit('update:modelValue', $event.target.value)"/>
  <!--if the given input is does't store the data property we will define some changes,
     when we use v-model in custome component it automatically receive prop call(modelvalue), 
  we need to specify in the props option. 
  next we need to bind the props to the value attribute of input element (:value="modelValue", this will be take care of value of the input)
  when we use v-model directive in custome component it automaticaly listen to an event called 'update:modelValue',
so the input element we bind to the input element and emit the update 'update:modelValue', then the data we passed to the parent is ($event.target.value)which is input element value-->
</template>
<script>
export default {
  name: 'Input-val',
  props: {
    modelValue: String      // here specify the props 
  }
}
</script>
<style scoped>
  Input[type='text'] {
    display: block;
    width: 400px;
    padding: 6px 12px;
    font-size: 14px;
    line-height: 1.4 ;
    color: #555;
    background-color:#fff ;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
</style>