<script setup>

</script>

<template>
  <v-responsive
      class="mx-auto"
      max-width="360"
  >
    <v-text-field
        hide-details="auto"
        variant="solo"
        placeholder="Anime"
        density="compact"
        clearable
        rounded
        flat
    >
      <template v-slot:append>
        <v-btn class="btn-agregar" flat rounded>
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
  background-color: red;
}
</style>