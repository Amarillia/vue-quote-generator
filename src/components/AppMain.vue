<template>

<div class="container">
    <h1>{{ msg }}</h1>
		<div class="jumbotron">
			<div class="row text-center">
				<div class="col-xs-6" id="quote-box">
					<p id="text"></p>
					<p id="author"></p>
            <Button id="new-quote" name="Press it for a new quote"/>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import Button from "./AppButton.vue";


export default {
  name: "Main",
  props: {
    msg: String
  },  components: {
    Button
  },
  mounted() {
    let recaptchaScript = document.createElement('script')
    recaptchaScript.setAttribute('src', 'https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js')
    document.head.appendChild(recaptchaScript)
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}

</style>
