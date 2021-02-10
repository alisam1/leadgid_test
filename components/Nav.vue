<template>
 <nav class="main-navigation">
  <button class="menu-toggle" @click="openMenu()" :class="{ '--active': isOpen }">Menu</button>
    <ul class="menu">
      <li><Nuxt-link to="/">Home</Nuxt-link></li>
      <li><Nuxt-link to="/about">About</Nuxt-link></li>
      <li><Nuxt-link to="/shop">Shop</Nuxt-link></li>
      <li><Nuxt-link to="/contact">Contact</Nuxt-link></li>
    </ul>
 </nav>
</template>
<script>
export default {
  name: 'Nav',
  data() {
    return {
        isOpen: false,
    }
  },
  methods: {
    openMenu(){
        this.isOpen = !this.isOpen;
    }
  }
}
</script>

<style>
</style>