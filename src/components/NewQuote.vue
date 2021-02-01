<template>
  <form>
    <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3">
      <div class="form-group">
        <label class="control-label">Quote</label>
        <textarea class="form-control" rows="3" v-model="quote"></textarea>
      </div>
    </div>
    <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3">
      <div class="form-group">
        <button class="btn btn-primary" @click.prevent="createNew">
          Add Quote
        </button>
      </div>
    </div>
  </form>
</template>

<script>
export default {
  data: function () {
    return { quote: "" };
  },
  methods: {
    createNew() {
      this.$emit("addQuoteEvent", this.quote);
      this.quote = "";
    },
  },
  beforeCreate() {
    console.log("[NewQuote.vue] beforeCreate");
  },
  created() {
    console.log("[NewQuote.vue] created");
  },
  beforeMount() {
    console.log("[NewQuote.vue] beforeMount");
  },
  mounted() {
    console.log("[NewQuote.vue] mounted");
  },
  beforeUpdate() {
    console.log("[NewQuote.vue] beforeUpdate");
  },
  updated() {
    console.log("[NewQuote.vue] updated");
  },
  beforeDestroy() {
    console.log("[NewQuote.vue] beforeDestroy");
  },
  destroyed() {
    console.log(" [NewQuote.vue]destroyed");
  },
};
</script>

<style scoped>
</style>