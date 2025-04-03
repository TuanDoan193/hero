<template>
  <div class="card">
    <div class="card-image-wrapper">
      <img v-if="imageUrl" :src="imageUrl" :alt="title" class="card-image" />
    </div>
    <div class="card-content">
      <h3 class="card-title">{{ title }}</h3>
      <p v-if="description" class="card-description">{{ description }}</p>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  title: string
  description?: string
  imageUrl?: string
}>()
</script>

<style scoped lang="scss">
.card {
  background: $background-body;
  border-radius: 0.5rem;
  box-shadow: 0 0.25rem 0.5rem rgba(0, 0, 0, 0.1);
  overflow: hidden;
  transition: transform 0.3s ease;

  &:hover {
    transform: translateY(-5px);
  }
  .card-image-wrapper {
    width: 100%;
    /* Modern browsers */
    aspect-ratio: 3 / 2;
    overflow: hidden;
    position: relative;
  }

  .card-image {
    width: 100%;
    height: 100%;
    object-fit: cover;
    position: absolute;
    top: 0;
    left: 0;
  }

  .card-content {
    padding: 1rem;
  }

  .card-title {
    font-size: 1.2rem;
    font-weight: bold;
    margin: 0;
  }

  .card-description {
    font-size: 1rem;
    color: $dark-color;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    overflow: hidden;
    text-overflow: ellipsis;
  }
}
</style>
