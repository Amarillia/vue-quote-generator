<template>
  <button variant="primary" class="genButton">
    {{ name }}
  </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    name: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.genButton {
    width: 200px;
    height: 50px;
    background-color: darkgreen;
    border: 1px solid darkgreen;
    color: #fff;
    padding: 10px 15px;
}
</style>
