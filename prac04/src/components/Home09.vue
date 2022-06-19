<template>
  Home09
  <p>Employee Name:</p> 
   <div>
     <p v-for="employee in employeeList" :key="employee">{{employee}}</p>
   </div>
</template>

<script>
import {ref} from 'vue';
export default {
  name: "Home09",
  setup(){
    const employeeList = ref([
      "AA",
      "BB",
      "CC",
      "DD"
    ]);
    return{
      employeeList
    }
  }
}
</script>

<style>

</style>