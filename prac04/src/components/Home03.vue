<template>
  Home03
  <p>Employee NAme : {{employeeName}}</p>
  <button @click="buttonClick">Click</button>
</template>

<script>
export default {
  name: "home03",
  setup(){
    let employeeName = "jenny";
    let age = 50;
    let isMarried = true;
    const buttonClick = () => {
      console.log(employeeName);
      console.log(age);
      console.log(isMarried);
    }
    return{
      employeeName: employeeName,
      age: age,
      isMarried: isMarried,
      buttonClick
    }
  }
}
</script>

<style>

</style>