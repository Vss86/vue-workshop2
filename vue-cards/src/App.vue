<template>
  <div class="card" @click="handleClick">
    <h2>{{ cardTitle }}</h2>
    <p>{{ cardContent }}</p>
  </div>
</template>

<script>
export default {
  props: {
    cardTitle: String,
    cardContent: String,
  },
  methods: {
    handleClick() {
      this.$emit('card-clicked', { title: this.cardTitle, content: this.cardContent });
    },
  },
};
</script>

<style scoped>
.card {
  border: 1px solid #ccc;
  padding: 20px;
  margin: 10px;
  border-radius: 5px;
  cursor: pointer;
}
</style>
