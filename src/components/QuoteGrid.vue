<template>
  <div class="row">
    <app-quote
      v-for="(quote, index) in quotes"
      :key="quote"
      @click.native="deleteQuote(index)"
    >
      <div class="panel panel-default">
        <div class="panel-body">{{ quote }}</div>
      </div>
    </app-quote>
  </div>
</template>

<script>
import Quote from "./Quote";

export default {
  props: ["quotes"],
  components: {
    appQuote: Quote,
  },
  methods: {
    deleteQuote(index) {
      this.$emit("deleteQuoteEvent", index);
    },
  },
};
</script>

<style scoped>
</style>