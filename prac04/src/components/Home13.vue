<template>
  Home13
  <Employees :employee-list="employeeList"/>
</template>

<script>
import {ref} from 'vue';
import Employees  from "./Employees.vue"
export default {
  components: {Employees},
  setup(){
    const employeeList = ref([
      {employId: 1, employeeName: "janny", age: 50},
      {employId: 3, employeeName: "ww", age: 2}
    ])

    return{
      employeeList
    }
  }
}
</script>

<style>

</style>