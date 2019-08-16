<template>
  <Button id="submit" name="Submit"/>
</template>

<script>
import Button from "./AppButton.vue";

export default {
  name: "Footer",
  props: {
    name: String
  },
  components: {
    Button
  }
};
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.quoteFooter {
  margin: 20px 0;
  background-color: darkgreen;
  color: #fff;
  height: 70px;
  bottom: 0;
  position: absolute;
  width: 100%;
}

.contactButton {
  width: 100px;
  text-align: center;
  border: 1px solid #fff;
  background-color: #fff;
  color: darkgreen;
  padding: 10px 20px;
  position: absolute;
  bottom: 15px;
  left: 100px;
}
</style>
