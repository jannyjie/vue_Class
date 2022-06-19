<template>
    <div v-for="emp in employeeList" :key="emp.employeeId" >
      <h3> {{emp.employeeId}} </h3>
      {{ emp.employeeName }}
      {{ emp.age }}
    </div>
    <p>
      Total Count : 
    </p>
</template>

<script>
import { computed } from "vue";
export default {
  props: ["employeeList"],
  setup(){
  
    return {  };
  }
};
</script>

<style>
</style>
