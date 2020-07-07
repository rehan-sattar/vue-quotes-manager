<template>
  <div class="container my-5">
    <QuotesProgressBar />
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
      this.quotes = this.quotes.concat(newQuote);
    }
  }
};
</script>

<style>
</style>
