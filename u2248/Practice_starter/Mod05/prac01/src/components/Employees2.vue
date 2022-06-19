<template>
    <div v-for="emp in employeeList" :key="emp.employeeId" >
      <h3> {{emp.employeeId}} </h3>
      {{ emp.employeeName }}
      {{ emp.age }}
    </div>
</template>

<script>

export default {
  props: ["employeeList"],
  setup() {
   
  },
};
</script>

<style>
</style>

