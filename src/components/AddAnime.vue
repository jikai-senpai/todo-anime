<script setup>
import {ref} from 'vue'

const btnAdd = () => {
  console.log('Botón clickeado')
}
</script>

<template>
  <v-responsive
      class="mx-auto"
      max-width="360"
  >
    <v-text-field
        class="input-anime"
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