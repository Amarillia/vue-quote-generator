<template>
  <div id="app">
    <Header headerTitle="Random Quote Generator" />
    <div class="container">
      <div class="jumbotron">
        <h1>"Generate random new quotes and brighten up your day."</h1>
        <div class="row text-center">
          <div class="col-xs-6" id="quote-box">
            <p id="text"></p>
            <p id="author"></p>
            <Button id="new-quote" name="Press it for a new quote" :onClick="quoteGen" />
            <a
              id="tweet-quote"
              class="twitter-share-button"
              name
              v-bind:href="url"
              data-show-count="false"
              target="_blank"
            ></a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./components/AppHeader";
import Button from "./components/AppButton";

export default {
  name: "app",
  components: {
    Header,
    Button
  },
  data() {
    return {
      url: "https://twitter.com/intent/tweet?text="
    };
  },
  methods: {
    quoteGen() {
      var quotes = [
        "Don't cry because it's over, smile because it happened.",
        "I'm selfish, impatient and a little insecure. I make mistakes, I am out of control and at times hard to handle. But if you can't handle me at my worst, then you sure as hell don't deserve me at my best.",
        "Be yourself; everyone else is already taken.",
        "You are never too old to set another goal or to dream a new dream.",
        "If you can dream it, you can do it.",
        "Never give up, for that is just the place and time that the tide will turn.",
        "Two things are infinite: the universe and human stupidity; and I'm not sure about the universe.",
        "Be who you are and say what you feel, because those who mind don't matter, and those who matter don't mind.",
        "A room without books is like a body without a soul.",
        "No one can make you feel inferior without your consent."
      ];

      var author = [
        "- Dr. Seuss",
        "- Marilyn Monroe",
        "- Oscar Wilde",
        "- C.S Lewis",
        "- Walt Disney",
        "- Harriet Beecher Stowe",
        "- Albert Einstein",
        "- Bernard M. Baruch",
        "- Marcus Tullius Cicero",
        "- Eleanor Roosevelt"
      ];

      function newQuoteGen() {
        var newQuote = Math.floor(Math.random() * quotes.length);
        var newAuthor = Math.floor(Math.random() * quotes.length);

        document.getElementById("text").innerHTML = quotes[newQuote];
        document.getElementById("author").innerHTML = author[newAuthor];
      }

      newQuoteGen();
    }
  },

  mounted() {
    let recaptchaScript = document.createElement("script");
    recaptchaScript.setAttribute(
      "src",
      "https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js"
    );
    document.head.appendChild(recaptchaScript);
    let tweetScript = document.createElement("script");
    // tweetScript.setAttribute("async");
    tweetScript.setAttribute("href", "/web/tweet-button");
    tweetScript.setAttribute("rel", "canonical");
    document.head.appendChild(tweetScript);
    this.quoteGen();
  }
};
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
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}

h1 {
  font-size: 20px;
  font-weight: 200;
}
.jumbotron {
  max-width: 70%;
  margin: 0 auto;
  background: #d0f0c0;
  padding: 15px;
  border-radius: 10px;
}

#text {
  font-size: 30px;
  font-weight: 500;
}

#author {
  font-size: 20px;
  font-weight: 500;
  text-align: right;
}

#new-quote {
  font-size: 20px;
  width: auto;
  border-radius: 10px;
  -webkit-box-shadow: 10px 10px 15px 0px rgba(0, 0, 0, 0.3);
  -moz-box-shadow: 10px 10px 15px 0px rgba(0, 0, 0, 0.3);
  box-shadow: 10px 10px 15px 0px rgba(0, 0, 0, 0.3);
}
#tweet-quote {
  display: flex;
  max-width: 50px;
  text-align: left;
  background: url("./assets/twitter-brands.svg") no-repeat;
  border: none;
  padding: 20px;
}
</style>
