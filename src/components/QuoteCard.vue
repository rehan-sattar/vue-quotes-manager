<template>
  <div class="card">
    <div class="card-body">
      <!-- {{}} -->
      Some text
    </div>
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