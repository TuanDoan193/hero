<template>
  <div class="default-layout">
    <header class="header">
      <div class="logo">
        <img src="@/assets/images/logoA.png" alt="Logo" />
        <span>Tuan Doan</span>
      </div>
      <div class="menu-toggle" @click="toggleMenu">☰</div>
      <nav class="menu" :class="{ active: isMenuActive }">
        <a href="#">Indie Game</a>
        <a href="#">Entry Game</a>
        <a href="#">Community</a>
      </nav>
    </header>
    <main>
      <slot></slot>
    </main>
    <footer>
      <p>&copy; 2025 Công ty ABC</p>
    </footer>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const isMenuActive = ref<boolean>(false)
const toggleMenu = (): void => {
  isMenuActive.value = !isMenuActive.value
}
</script>

<style scoped lang="scss">
.default-layout {
  display: flex;
  flex-direction: column;
  height: 100vh;
}

header,
footer {
  background-color: $background-secondary;
  color: $text-color-white;
  padding: 1rem;
  box-shadow: $box-shadow;
  padding: $spacing-unit 2rem;
}

main {
  flex: 1;
  padding: 1rem;
  margin-top: 3rem;
}

.header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;

  z-index: 1000;

  .logo {
    display: flex;
    align-items: center;
    font-size: 1.2rem;
    font-weight: bold;
    font-family: $font-family-base;

    img {
      height: 1rem;
      margin-right: 0.5rem;
    }
  }

  .menu {
    display: flex;
    gap: $spacing-unit;

    a {
      padding: 0.5rem 1.2rem;
      border: 1px solid $text-color-white;
      border-radius: 0.5rem;
      color: $text-color-white;
      text-decoration: none;
      font-size: 1.2rem;
      font-weight: 500;
      transition: all 0.3s ease;

      &:hover {
        background-color: rgba(255, 255, 255, 0.2);
      }
    }
  }

  .menu-toggle {
    display: none;
    font-size: 2rem;
    cursor: pointer;
  }

  @include respond-to('sm') {
    .menu {
      display: none;
      flex-direction: column;
      position: absolute;
      top: 100%;
      right: 0;
      background: $background-secondary;
      width: 100%;
      text-align: right;
      padding: 1rem;
      box-shadow: 0 0.2rem 0.4rem rgba(0, 0, 0, 0.1);

      a {
        display: block;
        padding: 0.8rem;
        text-align: center;
      }
    }

    .menu.active {
      display: flex;
      gap: 1rem;
    }

    .menu-toggle {
      display: block;
    }
  }
}
</style>
