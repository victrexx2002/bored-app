<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
  <header>
  <h1> Unbored </h1>

  <nav>
    <RouterLink to="/" class="link"><button>Home</button></RouterLink>
    <RouterLink to="/about" class="link"><button>about</button></RouterLink>
  </nav>
  </header>

  <RouterView />
</template>


<style lang="scss" scoped>
header{  
    padding: 1rem 0;
    display: flex;
    justify-content: space-between;

    nav{
      display: flex;
      gap: 1rem;

      .link{
        text-decoration: none;
        color: inherit;
      }
    }

  }
</style>
