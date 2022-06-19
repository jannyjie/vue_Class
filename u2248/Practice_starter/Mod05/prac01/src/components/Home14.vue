<template>
  <h1>Home</h1>
  <button >Show/Hide Employees</button>
 
</template>
<script>
import { ref } from "vue";

export default {
  name: "Home14",
  components: {  },
  setup() {
    const employeeList = ref([
      { employeeId: 1, employeeName: "mary", age: 50 },
      { employeeId: 2, employeeName: "candy", age: 60 },
      { employeeId: 3, employeeName: "lulu", age: 40 },
    ]);
  
    return {
      employeeList,

    };
  },
};
</script>

<style>
</style>


