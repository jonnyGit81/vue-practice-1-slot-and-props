<template>
  <div class="container">
    <app-pogress
      :quoteCount="quotes.length"
      :maxQuotes="maxQuotes"
    ></app-pogress>
    <app-new-quote @addQuoteEvent="addQuoteEventListener"></app-new-quote>

    <app-quote-grid
      @deleteQuoteEvent="deleteQuoteEventListener"
      :quotes="quotes"
    ></app-quote-grid>

    <div class="row">
      <div class="col-md-12 alert alert-info text-center">
        <label> Click the Quote for delete </label>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid";
import NewQuote from "./components/NewQuote";
import Pogress from "./components/Pogress";
export default {
  data: function () {
    return {
      quotes: ["First Quote"],
      maxQuotes: 10,
    };
  },
  methods: {
    addQuoteEventListener(data) {
      if (this.quotes.length < this.maxQuotes) {
        this.quotes.push(data);
      } else {
        alert("quotes full, please delete some quotes");
      }
    },
    deleteQuoteEventListener(data) {
      this.quotes.splice(data, 1);
    },
  },
  components: {
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote,
    appPogress: Pogress,
  },
  beforeCreate() {
    console.log("[App.vue] beforeCreate");
  },
  created() {
    console.log("[App.vue] created");
  },
  beforeMount() {
    console.log("[App.vue] beforeMount");
  },
  mounted() {
    console.log("[App.vue] mounted");
  },
  beforeUpdate() {
    console.log("[App.vue] beforeUpdate");
  },
  updated() {
    console.log("[App.vue] updated");
  },
  beforeDestroy() {
    console.log("[App.vue] beforeDestroy");
  },
  destroyed() {
    console.log(" [App.vue]destroyed");
  },
};
</script>


<style>
</style>
