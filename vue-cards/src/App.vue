<template>
  <div id="app">
    <BaseLayout>
      <template #header>
        <h1>Fotbollsklubbar i Europa</h1>
      </template>
      <template #main>
        <div>
          <Card
            v-for="club in footballClubs"
            :key="club.id"
            :cardData="club"
          >
            <template #button>
              <button @click="handleCardClick(club)">Watch {{ club.name }}</button>
            </template>
          </Card>
        </div>
      </template>
      <template #footer>
        <p>&copy; 2023 Fotbollsklubbar AB</p>
      </template>
    </BaseLayout>
  </div>
</template>

<script lang="ts">
import BaseLayout from "@/components/BaseLayout.vue";
import Card from "@/components/Card.vue";

export default {
  components: {
    BaseLayout,
    Card,
  },
  data() {
    return {
      footballClubs: [
        
        { id: 1, name: "Arsenal", country: "England" },
        { id: 2, name: "FC Barcelona", country: "Spain" },
        { id: 3, name: "Real Madrid", country: "Spain" },
        { id: 4, name: "Bayern Munich", country: "Germany" },
        { id: 5, name: "Paris Saint-Germain", country: "France" },
        { id: 6, name: "Juventus", country: "Italy" },
        { id: 7, name: "Liverpool", country: "England" },
        { id: 8, name: "AC Milan", country: "Italy" },
        { id: 9, name: "Ajax", country: "Netherlands" },
        { id: 10, name: "Porto", country: "Portugal" },
      ],
    };
  },
  methods: {
    handleCardClick(club) {
      alert(`Watching ${club.name}`);
    },
  },
};
</script>

<style>
#app {
  text-align: center;
  margin-top: 60px;
}
</style>
