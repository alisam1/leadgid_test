<template>
  <header class="site-header">
    <div class="site-branding">
      <h1 class="site-title"><a href="/" rel="home">LeadGid</a></h1>
        <h2 class="site-description">Test HTML Template</h2>
    </div>
    <Nav/>
  </header>
</template>

<script>
import Nav from '~/components/Nav.vue';
export default {
  name: 'Header',
  components: { 
      Nav
  },
  data() {
    return {
      isOpen: false,
    }
  },
}
</script>

<style>
</style>
