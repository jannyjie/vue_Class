<template>
  <h1>Home</h1>
  <div ref="div">
    <p>Employee Name : {{ employeeName }}</p>
    <p>Age : {{ age }}</p>
    <p>Is Married : {{ isMarried }}</p>
  </div>
  <button @click="buttonClick">Click</button>
  <hr />
  <div>
    Employee Name : <input type="text" v-model="employeeName" /> <br />
    age : <input type="number" v-model="age" /><br />
    isMarried : <input type="checkbox" v-model="isMarried" /><br />
  </div>
</template>

<script>
import { ref  } from "vue";
export default {
  name: "Home7",
  setup() {
    const employee =  {
      employeeName: "mary",
      age: 50,
      isMarried: true,
    } ;


    const div = ref(null);
    const buttonClick = () => {
      employeeName = "candy";
      age= 60;
      isMarried = false;
      console.log(employeeName);
      console.log(age);
      console.log(isMarried);
      div.value.style.backgroundColor = "yellow";
    };

    return {
      employee,
      buttonClick,
      div,
    };
  },
};
</script>

<style>
</style>

