<template>
  <div class="card mt-3 quotes__card" @click="emitDeleteEvent(quote.id)">
    <div class="card-body">{{ quote.text }}</div>
  </div>
</template>

<script>
export default {
  name: "QuoteCard",
  props: {
    quote: {
      type: Object
    }
  },
  methods: {
    emitDeleteEvent(quoteId) {
      this.$emit("deleteQuote", quoteId);
    }
  }
};
</script>

<style scoped>
.quotes__card:hover {
  background-color: red;
  opacity: 0.4;
  cursor: pointer;
  color: #ffff;
}
</style>