<script setup>
const props = defineProps({
  myPropAnime: {
    type: String,
    required: true
  }
})

const emit = defineEmits(['deleteAnime'])

const handleDelete = () => {
  emit('deleteAnime', props.myPropAnime)
}
</script>

<template>
  <v-card>
    <v-card-title>{{ props.myPropAnime }}</v-card-title>
    <v-btn class="btn-delete" @click="handleDelete" color="red">Eliminar</v-btn>
  </v-card>
</template>

<style scoped>
.btn-delete {
  margin-left: auto;
}
</style>