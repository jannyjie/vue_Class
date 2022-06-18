<template>
<div class="card">
     <slot name="header"></slot>
      <slot></slot>
    <slot name="footer"></slot>
  </div>
</template>

<script>
export default {
    name: 'NameCard'
}
</script>
<style scoped>
.card{
    border: solid 1px #000;
    width: 300px;
}
</style>