<template>
  <h1>Home</h1>
  
  keyword : <input type="text"  />
  <p>filter Keyword - </p>
  <hr/>
  <p>Employee Name :</p>
  <div>
    <p v-for="employee in employeeList" :key="employee">{{ employee }}</p>
  </div>
</template>
<script>
import { ref } from "vue";
export default {
  name: "Home10",
  setup() {

    const employeeList = ref([
      "mary",
      "candy",
      "lulu",
      "cindy",
      "joy",
      "christine",
    ]);
    
    return {
      employeeList,
   
    };
  },
};
</script>

<style>
</style>
