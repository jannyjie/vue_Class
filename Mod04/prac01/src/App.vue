<template>
  <div class="container">
    <ul class="nav justify-content-center">
      <li class="nav-item">
        <router-link to="/">Home</router-link>
      </li>
      <li class="nav-item">
        <router-link to="/about">about</router-link>
      </li>
    </ul>
  </div>
  <div class="container">
    	<router-view></router-view>
  </div>
</template>

<script>

export default {
  name: "App",
};
</script>

<style>
#app {
  color: #2c3e50;
  background-color: rgb(252, 233, 198);
  padding: 50px;
}
.active {
    color: red;
}
body {
  background-color: rgb(252, 233, 198) !important;
}

</style>
