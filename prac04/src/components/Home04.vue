<template>
  Home04
  <p>Employee NAme : {{employeeName}}</p>
  <button @click="buttonClick">Click</button>
</template>

<script>
import {ref} from 'vue';
export default {
  name: "home04",
  setup(){
    let employeeName = ref("jenny");
    let age = ref(50);
    let isMarried = ref(true);
    const buttonClick = () => {
      employeeName.value = 'jack'
      age.value = 30
      isMarried.value = false
      console.log(employeeName.value);
      console.log(age.value);
      console.log(isMarried.value);
    }
    return{
      employeeName: employeeName,
      age: age,
      isMarried: isMarried,
      buttonClick
    }
  }
}
</script>

<style>

</style>