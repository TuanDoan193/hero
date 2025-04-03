<script setup lang="ts">
import Card from '@/components/SmileCard.vue'
import BearImage from '@/assets/images/bear.png'
import Woman from '@/assets/images/woman.jpg'

const cards = [
  { title: 'Indie Game', description: 'Discover the best indie games.', imageUrl: BearImage },
  {
    title: 'Entry Game',
    description: 'Get started with beginner-friendly games.',
    imageUrl: Woman,
  },
  { title: 'Community', description: 'Join the gaming community.', imageUrl: Woman },
  {
    title: 'Indie Game',
    description:
      'A thrilling adventure through uncharted worlds. Dive into a universe of creativity, where every choice you make shapes your journey. Explore, battle, and conquer in this unique indie experience.',
    imageUrl: BearImage,
  },
  {
    title: 'Indie Game',
    description:
      'Cutting-edge technology meets user-friendly design. Discover the future of innovation with our latest product, built to enhance your everyday life.',
    imageUrl: Woman,
  },
  {
    title: 'Indie Game',
    description:
      'Where imagination meets functionality. Our creative designs are crafted to inspire and transform the way you interact with the digital world.',
    imageUrl: BearImage,
  },
  {
    title: 'Indie Game',
    description:
      'Unlock your full potential. Take the first step toward personal growth and self-improvement with our curated resources, expert guidance, and community support.',
    imageUrl: Woman,
  },
  { title: 'Indie Game', description: 'Discover the best indie games.', imageUrl: BearImage },
  {
    title: 'Indie Game',
    description:
      'Unlock your full potential. Take the first step toward personal growth and self-improvement with our curated resources, expert guidance, and community support.',
    imageUrl: Woman,
  },
  { title: 'Indie Game', description: 'Discover the best indie games.', imageUrl: BearImage },
  { title: 'Indie Game', description: 'Discover the best indie games.', imageUrl: Woman },
  {
    title: 'Indie Game',
    description:
      'Uncover the beauty of the world with our exclusive travel packages. From breathtaking landscapes to immersive cultural experiences, every journey promises unforgettable memories..',
    imageUrl: BearImage,
  },
  { title: 'Indie Game', description: 'Discover the best indie games.', imageUrl: BearImage },
  {
    title: 'Entry Game',
    description: 'Get started with beginner-friendly games.',
    imageUrl: Woman,
  },
  { title: 'Community', description: 'Join the gaming community.', imageUrl: Woman },
  {
    title: 'Indie Game',
    description:
      'A thrilling adventure through uncharted worlds. Dive into a universe of creativity, where every choice you make shapes your journey. Explore, battle, and conquer in this unique indie experience.',
    imageUrl: BearImage,
  },
  {
    title: 'Indie Game',
    description:
      'Cutting-edge technology meets user-friendly design. Discover the future of innovation with our latest product, built to enhance your everyday life.',
    imageUrl: Woman,
  },
  {
    title: 'Indie Game',
    description:
      'Where imagination meets functionality. Our creative designs are crafted to inspire and transform the way you interact with the digital world.',
    imageUrl: BearImage,
  },
  {
    title: 'Indie Game',
    description:
      'Unlock your full potential. Take the first step toward personal growth and self-improvement with our curated resources, expert guidance, and community support.',
    imageUrl: Woman,
  },
  { title: 'Indie Game', description: 'Discover the best indie games.', imageUrl: BearImage },
  {
    title: 'Indie Game',
    description:
      'Unlock your full potential. Take the first step toward personal growth and self-improvement with our curated resources, expert guidance, and community support.',
    imageUrl: Woman,
  },
  { title: 'Indie Game', description: 'Discover the best indie games.', imageUrl: BearImage },
  { title: 'Indie Game', description: 'Discover the best indie games.', imageUrl: Woman },
  {
    title: 'Indie Game',
    description:
      'Uncover the beauty of the world with our exclusive travel packages. From breathtaking landscapes to immersive cultural experiences, every journey promises unforgettable memories..',
    imageUrl: BearImage,
  },
  {
    title: 'Indie Game',
    description:
      'A thrilling adventure through uncharted worlds. Dive into a universe of creativity, where every choice you make shapes your journey. Explore, battle, and conquer in this unique indie experience.',
    imageUrl: BearImage,
  },
  {
    title: 'Indie Game',
    description:
      'Cutting-edge technology meets user-friendly design. Discover the future of innovation with our latest product, built to enhance your everyday life.',
    imageUrl: Woman,
  },
  {
    title: 'Indie Game',
    description:
      'A thrilling adventure through uncharted worlds. Dive into a universe of creativity, where every choice you make shapes your journey. Explore, battle, and conquer in this unique indie experience.',
    imageUrl: BearImage,
  },
  {
    title: 'Indie Game',
    description:
      'Cutting-edge technology meets user-friendly design. Discover the future of innovation with our latest product, built to enhance your everyday life.',
    imageUrl: Woman,
  },
  {
    title: 'Indie Game',
    description:
      'A thrilling adventure through uncharted worlds. Dive into a universe of creativity, where every choice you make shapes your journey. Explore, battle, and conquer in this unique indie experience.',
    imageUrl: BearImage,
  },
  {
    title: 'Indie Game',
    description:
      'Cutting-edge technology meets user-friendly design. Discover the future of innovation with our latest product, built to enhance your everyday life.',
    imageUrl: Woman,
  },
]
</script>

<template>
  <div class="home">
    <Card
      v-for="(card, index) in cards"
      :key="index"
      :title="card.title"
      :description="card.description"
      :imageUrl="card.imageUrl"
    />
  </div>
</template>

<style scoped lang="scss">
.home {
  @include responsive-grid();
}
</style>
