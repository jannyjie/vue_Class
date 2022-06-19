<template>
  Home10
  <p>Employee Name:</p> 
    <input type="text" name="" v-model="keyword" id="">
   <div>
     <p v-for="employee in filterResult" :key="employee">{{employee}}</p>
   </div>
</template>

<script>
import {computed, ref} from 'vue';
export default {
  name: "Home10",
  setup(){
    const keyword = ref("")
    const employeeList = ref([
      "AA",
      "BB",
      "CC",
      "DD"
    ]);

    const filterResult = computed(() => {
      return employeeList.value.filter((name) => name.startsWith(keyword.value));
    })
    return{
      employeeList,
      filterResult,
      keyword
    }
  }
}
</script>

<style>

</style>