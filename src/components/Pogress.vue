<template>
  <div class="row">
    <div class="div col-sm-12">
      <h3>Quotes Addes</h3>
      <div class="progress">
        <div
          class="progress-bar"
          role="progressbar"
          :style="{ width: (quoteCount / maxQuotes) * 100 + '%' }"
          :aria-valuenow="quoteCount"
          aria-valuemin="0"
          aria-valuemax="100"
        >
          {{ quoteCount * 10 }}%
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["quoteCount", "maxQuotes"],
};
</script>