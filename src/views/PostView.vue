<template>
    <h1>Sección de Post elemento: {{ postId }}</h1>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue';
import { useRoute } from 'vue-router';

let postId = ref();

onMounted(() => {
    const route = useRoute();
    postId.value = route.params.id;
})
</script>

<style scoped lang="scss"></style>