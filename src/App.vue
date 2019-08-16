<template>
  <div id="app">
    <Header headerTitle="Random Quote Generator"/>
    <Main msg="This is a webpage to generate some random new quotes and brighten up your day."/>
    <Footer name="Contact"/>

  </div>
</template>

<script>
import Main from "./components/AppMain.vue";
import Footer from "./components/AppFooter.vue";
import Header from "./components/AppHeader.vue";

export default {
  name: "app",
  components: {
    Main,
    Footer,
    Header
  }
};

// var quotes = ["Don't cry because it's over, smile because it happened.", "I'm selfish, impatient and a little insecure. I make mistakes, I am out of control and at times hard to handle. But if you can't handle me at my worst, then you sure as hell don't deserve me at my best.", "Be yourself; everyone else is already taken.", "You are never too old to set another goal or to dream a new dream.", "If you can dream it, you can do it.", "Never give up, for that is just the place and time that the tide will turn.", "Two things are infinite: the universe and human stupidity; and I'm not sure about the universe.", "Be who you are and say what you feel, because those who mind don't matter, and those who matter don't mind.", "A room without books is like a body without a soul.", "No one can make you feel inferior without your consent."];

	// var author = ["- Dr. Seuss","- Marilyn Monroe","- Oscar Wilde","- C.S Lewis", "- Walt Disney", "- Harriet Beecher Stowe","- Albert Einstein","- Bernard M. Baruch","- Marcus Tullius Cicero","- Eleanor Roosevelt"];

// function newQuoteGen() {
	// var newQuote = Math.floor(Math.random() * quotes.length);
	// var newAuthor = Math.floor(Math.random() * quotes.length);

	// document.getElementById('text').innerHTML = quotes[newQuote];
	// document.getElementById('author').innerHTML = author[newAuthor];

// }

// newQuoteGen();

</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Roboto+Condensed");

html,
body {
  font-family: "Roboto Condensed", sans-serif;
  background-color: darkseagreen;
}

#app {
  font-family: "Roboto Condensed", sans-serif;
  /* font-family: "Avenir", Helvetica, Arial, sans-serif; */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
