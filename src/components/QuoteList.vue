<template>
  <div class="row">
    <div class="col text-center" v-if="quotes.length === 0">
      <h2>No Quotes!</h2>
    </div>
    <div class="col-md-4 col-lg-4 col-sm-12" v-for="quote in quotes" :key="quote.id">
      <QuoteCard :quote="quote" @deleteQuote="forwardDeleteEventToParent" />
    </div>
  </div>
</template>

<script>
import QuoteCard from "./QuoteCard";

export default {
  name: "QuoteList",
  props: {
    quotes: {
      type: Array,
      required: true
    }
  },
  components: {
    QuoteCard
  },
  methods: {
    forwardDeleteEventToParent(quoteId) {
      this.$emit("onDeletQuote", quoteId);
    }
  }
};
</script>