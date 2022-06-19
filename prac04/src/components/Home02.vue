<template>
  Home02
  <p>Employee NAme : {{employeeName}}</p>
</template>

<script>
export default {
  name: "home02",
  setup(){
    let employeeName = "jenny";
    let age = 50;
    let isMarried = true;

    return{
      employeeName: employeeName,
      age: age,
      isMarried: isMarried
    }
  }
}
</script>

<style>

</style>