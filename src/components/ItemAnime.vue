<script setup>
defineProps({
  myPropAnime: {
    type: String,
    required: true
  }
})
</script>

<template>
  <v-card>
    <v-card-title>{{ myPropAnime }}</v-card-title>
  </v-card>
</template>

<style scoped>

</style>