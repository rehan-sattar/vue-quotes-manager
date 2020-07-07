<template>
  <div>
    <h3>Quotes Added</h3>
    <div class="progress mt-3">
      <div
        class="progress-bar"
        role="progressbar"
        aria-valuenow="0"
        aria-valuemin="0"
        aria-valuemax="100"
        :style="{width: calcualteProgress + '%' }"
      >{{ totalQuotes}}/ 10</div>
    </div>
    <hr />
  </div>
</template>

<script>
export default {
  name: "QuotesProgressBar",
  props: {
    totalQuotes: Number
  },
  computed: {
    calcualteProgress() {
      return (this.totalQuotes / 10) * 100;
    }
  }
};
</script>