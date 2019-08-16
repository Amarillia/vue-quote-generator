<template>
  <div class="header">
    <h1>{{ headerTitle }}</h1> 
  </div>
</template>

<script>
export default {
  name: 'Header',
  props: {
    headerTitle: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  margin: 40px;
  color: darkgreen;
  font-size: 35px;
}
</style>
