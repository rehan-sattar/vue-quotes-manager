<template>
  <div class="container my-5">
    <QuotesProgressBar :totalQuotes="quotes.length" />
    <QuoteForm :addQuote="addQuote" />
    <QuoteList :quotes="quotes" />
  </div>
</template>

<script>
import QuotesProgressBar from "./components/QuotesProgressBar";
import QuoteForm from "./components/QuoteForm";
import QuoteList from "./components/QuoteList";

export default {
  components: {
    QuotesProgressBar,
    QuoteForm,
    QuoteList
  },
  data() {
    return {
      quotes: []
    };
  },
  methods: {
    addQuote(newQuote) {
      if (this.quotes.length < 10) {
        this.quotes = this.quotes.concat(newQuote);
      } else {
        alert("Sorry! You can't add more quotes!");
      }
    }
  }
};
</script>

<style>
</style>
