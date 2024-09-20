<script setup>
import DataAnime from "./DataAnime.vue";
import {ref} from 'vue'

const animeItems = ref([])
const animeName = ref('')

const btnAdd = () => {
  console.log(animeName.value)
  animeItems.value.push(animeName.value)
  animeName.value = ''
}
</script>

<template>
  <v-responsive
      class="mx-auto"
      max-width="360"
  >
    <v-text-field
        v-model="animeName"
        @keyup.enter="btnAdd"
        hide-details="auto"
        variant="solo"
        placeholder="Anime"
        density="compact"
        clearable
        rounded
        flat
    >
      <template v-slot:append>
        <v-btn
            class="btn-agregar"
            flat
            rounded
            @click="btnAdd"
        >
          Agregar
        </v-btn>
      </template>
    </v-text-field>
  </v-responsive>
</template>

<style scoped>
.btn-agregar {
  text-transform: none;
  color: #fff;
  background-color: #006adc;
}
</style>