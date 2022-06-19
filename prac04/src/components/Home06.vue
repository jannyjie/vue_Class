<template>
  Home06
  <div ref="div">
    <p>Employee NAme : {{ employeeName }}</p>
    <p>age: {{age}}</p>
    <p>inMarried : {{isMarried}}</p>
    <button @click="buttonClick">Click</button>
  </div>
  <hr/>
  <div>
    Employee Name: <input type="text" name="" v-model="employeeName" id="">
    age: <input type="text" name="" v-model="age" id="">
    inMarried : <input type="checkbox" name="" v-model="isMarried" id="">
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "home06",
  setup() {
    let employeeName = ref("jenny");
    let age = ref(50);
    let isMarried = ref(true);

    const div = ref(null)
    const buttonClick = () => {
      employeeName.value = "jack";
      age.value = 30;
      isMarried.value = false;
      console.log(employeeName.value);
      console.log(age.value);
      console.log(isMarried.value);
      div.value.style.backgroundColor = "yellow";
    };
    return {
      employeeName: employeeName,
      age: age,
      isMarried: isMarried,
      buttonClick,
      div
    };
  },
};
</script>

<style>
</style>