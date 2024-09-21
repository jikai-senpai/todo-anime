<script setup>
import {ref} from "vue";
import ItemAnime from "./ItemAnime.vue";

defineProps({
  animeItems: {
    type: Array,
    required: true
  }
})
</script>

<template>
  <div class="container-li">
    <h3>Lista de animes</h3>
    <div class="lista_anime">
      <ul>
        <li v-for="variableBucleAnime in animeItems" :key="variableBucleAnime">
          <ItemAnime :my-prop-anime="variableBucleAnime"/>
        </li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.container-li {
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.lista_anime ul {
  list-style-type: none;
  padding: 0;
}

.lista_anime li {
  margin: 5px 0;
}
</style>