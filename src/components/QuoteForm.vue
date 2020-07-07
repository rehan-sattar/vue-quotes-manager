<template>
  <div class="row justify-content-center mt-4">
    <div class="col-md-6 col-lg-5 col-sm-12">
      <form @submit="handleSubmit">
        <div class="form-group">
          <label for="quotesInput">
            <h3>New Quote</h3>
          </label>
          <textarea
            id="quotesInput"
            class="form-control"
            rows="4"
            placeholder="Enter your quote here..."
            v-model="quoteText"
            required
          ></textarea>
          <br />
          <button class="btn btn-primary btn-block">Add New Quote</button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
import { v4 as uuidv4 } from "uuid";

export default {
  name: "QuoteForm",
  data() {
    return {
      quoteText: ""
    };
  },
  props: {
    addQuote: {
      type: Function,
      required: true
    }
  },
  methods: {
    handleSubmit(event) {
      event.preventDefault();
      const newQuote = {
        id: uuidv4(),
        text: this.quoteText
      };
      this.addQuote(newQuote);
      this.quoteText = "";
    }
  }
};
</script>