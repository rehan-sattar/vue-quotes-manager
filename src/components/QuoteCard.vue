<template>
  <div class="card mt-3">
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
  }
};
</script>