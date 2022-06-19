<template>
  Home14
  <button @click="employeeList.pop()">Remove Employee</button>
  <button @click="show = !show">show/Hide</button>
  <Employees2 v-if="show" :employee-list="employeeList"/>
</template>

<script>
import {ref} from 'vue';
import Employees2  from "./Employees2.vue";
export default {

  
  components: {Employees2},
  setup(){
    const employeeList = ref([
      {employId: 1, employeeName: "janny", age: 50},
      {employId: 3, employeeName: "ww", age: 2}
    ]);

    const show = ref(true);


    return{
      employeeList,
      show
    }
  }
}
</script>

<style>

</style>