<script setup>
import AddAnime from "./components/AddAnime.vue";
import ListAnime from "./components/ListAnime.vue";
</script>

<template>
  <v-container>
        <h1 class="display-1 text-center title-list">Anime</h1>
        <div>
          <AddAnime/>
          <ListAnime/>
        </div>
  </v-container>
</template>

<style scoped>
.title-list {
  margin-top: 20px;
  padding-bottom: 20px;
}
</style>