<template>
  <div class="container my-5">
    <QuotesProgressBar />
    <QuoteForm />
  </div>
</template>

<script>
import QuotesProgressBar from "./components/QuotesProgressBar";
import QuoteForm from "./components/QuoteForm";

export default {
  components: {
    QuotesProgressBar,
    QuoteForm
  }
};
</script>

<style>
</style>
