<template>
  <div class="panel-body col-sm-3 col-xs-2 col-md-4 quote">
    <slot></slot>
  </div>
</template>
<script>
export default {
  beforeCreate() {
    console.log("[Quote.vue] beforeCreate");
  },
  created() {
    console.log("[Quote.vue] created");
  },
  beforeMount() {
    console.log("[Quote.vue] beforeMount");
  },
  mounted() {
    console.log("[Quote.vue] mounted");
  },
  beforeUpdate() {
    console.log("[Quote.vue] beforeUpdate");
  },
  updated() {
    console.log("[Quote.vue] updated");
  },
  beforeDestroy() {
    console.log("[Quote.vue] beforeDestroy");
  },
  destroyed() {
    console.log(" [Quote.vue]destroyed");
  },
};
</script>
<style scoped>
.panel-body {
  font-family: "Arizonia", sans-serif;
  font-size: 24px;
  color: #6e6e6e;
}

.quote {
  cursor: pointer;
}

.quote:hover {
  background-color: #ffe2e2;
}
</style>