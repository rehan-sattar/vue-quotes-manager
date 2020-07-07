<template>
  <div class="container my-5">
    <QuotesProgressBar :totalQuotes="quotes.length" />
    <QuoteForm :addQuote="addQuote" />
    <QuoteList :quotes="quotes" @onDeletQuote="deleteQuote" />
    <div class="alert alert-primary mt-5" role="alert">
      <b>Info:</b> Clicking any quote will remove that quote.
    </div>
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
    },
    deleteQuote(quoteId) {
      this.quotes = this.quotes.filter(q => q.id !== quoteId);
    }
  }
};
</script>

<style>
</style>
