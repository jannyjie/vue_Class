<template>
  Home12
  <p>Employee Name:</p> 
    <input type="text" name="" v-model="keyword" id="">
   <div>
     <p v-for="employee in filterResult" :key="employee">{{employee}}</p>
   </div>
   <button @click="buttonClick">Disable All Watch</button>
</template>

<script>
import {computed, ref, watch, watchEffect} from 'vue';
export default {
  name: "Home12",
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

    const disableWatch = watch(keyword, () => {
      console.log(`watch`, keyword.value);
    });

    const disbleWatchEffect = watchEffect(() => {
      console.log(`watchEffect`, keyword.value);
    })

    const buttonClick = () => {
      disableWatch();
      disbleWatchEffect();
    }
    return{
      employeeList,
      filterResult,
      keyword,
      buttonClick
    }
  }
}
</script>

<style>

</style>