<script setup>
import {ref} from 'vue'
import AddAnime from "./components/AddAnime.vue";
import ListAnime from "./components/ListAnime.vue";

const animeItems = ref([])

const handleAddAnime = (animeName) => {
  animeItems.value.push(animeName)
}
</script>

<template>
  <v-container>
    <h1 class="display-1 text-center title-list">Anime</h1>
    <div>
      <AddAnime @add-anime="handleAddAnime"/>
      <ListAnime :anime-items="animeItems"/>
    </div>
  </v-container>
</template>

<style scoped>
.title-list {
  margin-top: 20px;
  padding-bottom: 20px;
}
</style>