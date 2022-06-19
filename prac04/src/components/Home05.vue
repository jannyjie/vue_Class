<template>
  Home05
  <div ref="div">
    <p>Employee NAme : {{ employeeName }}</p>
    <button @click="buttonClick">Click</button>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "home05",
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