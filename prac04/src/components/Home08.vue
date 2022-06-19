<template>
  Home08
  <div ref="div">
    <p>Employee NAme : {{ employee.employeeName }}</p>
    <p>age: {{employee.age}}</p>
    <p>inMarried : {{employee.isMarried}}</p>
    <button @click="buttonClick">Click</button>
  </div>
  <hr/>
  <div>
    Employee Name: <input type="text" name="" v-model="employee.employeeName" id="">
    age: <input type="text" name="" v-model="employee.age" id="">
    inMarried : <input type="checkbox" name="" v-model="employee.isMarried" id="">
  </div>
  <hr/>
  <div>Employee Info : {{employeeInfo}}</div>
</template>

<script>
import { computed, reactive, ref } from "vue";
export default {
  name: "home08",
  setup() {
    const employee = reactive({
      employeeName : 'candy',
      age : 50,
      isMarried: true
    })

    const employeeInfo = computed(() => {
      return `${employee.employeeName} - ${employee.age} - ${employee.isMarried}`
    })

    const div = ref(null)
    const buttonClick = () => {
      employee.employeeName = "jack";
      employee.age = 30;
      employee.isMarried = false;
      console.log(employee.employeeName);
      console.log(employee.age);
      console.log(employee.isMarried);
      div.value.style.backgroundColor = "yellow";
    };
    return {
      employee,
      buttonClick,
      div,
      employeeInfo
    };
  },
};
</script>

<style>
</style>