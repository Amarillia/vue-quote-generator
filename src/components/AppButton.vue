<template>
  <button variant="primary" class="genButton Button" @click="onClick">
    <slot>{{ name }}</slot>
  </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    name: String,
    onClick: {
      type: Function,
      required: true
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<!-- https://codeburst.io/creating-reusable-components-with-vue-js-button-component-503167facfde -->

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
