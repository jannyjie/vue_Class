<template>
  <div v-for="emp in employeeList" :key="emp.employeeId">
    <h3>{{emp.employeeId}}</h3>
    {{emp.employeeName}}
    {{emp.age}}
  </div>
  <p>Total Count: {{Count}}</p>
</template>

<script>
import { computed, onBeforeUpdate, onMounted, onUnmounted } from 'vue'
export default {
    name:"Employees2",
    props: ["employeeList"],
    setup(props){
        console.log(props);
        const Count = computed(() => {
            return `${props.employeeList.length}`;
        })

        onMounted(() => {
          console.log("onMounteds");
        })

        onUnmounted(()=> {
          console.log("onUnmounted");
        })

        onBeforeUpdate(() => {
          console.log("onBeforeUpdate");
        })

        return{
            Count
        }
    }
}
</script>

<style>

</style>