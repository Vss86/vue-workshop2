<template>
  <div class="card">
    <h2>{{ cardData.name }}</h2>
    <p>Country: {{ cardData.country }}</p>
    <slot name="button">
      <button @click="emitCardClick">Click me!</button>
    </slot>
  </div>
</template>

<script>
export default {
  props: {
    cardData: {
      type: Object,
      required: true,
    },
  },
  methods: {
    emitCardClick() {
      alert(`Clicked on ${this.cardData.name}`);
    },
  },
};
</script>

<style scoped>
.card {
  border: 1px solid #ccc;
  padding: 10px;
  margin: 10px;
}
</style>
