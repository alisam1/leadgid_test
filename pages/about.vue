<template>
  <div id="page_about">
    <div class="container">
      <Header />
      <div id="content_about" class="site-content">
       <h1>About</h1>
      </div>
    </div>
    <Footer />
  </div>
</template>
<script>
import Header from '~/components/Header.vue';
import Footer from '~/components/Footer.vue'
export default {
  components: { 
    Header,
    Footer
  },
  name: 'about',
  data() {
    return {
    }
  },
}
</script>

<style lang="scss" scoped>
   #page_about > .container
   {
     height: 90vh;
   }
    h1{
      color: #333333;
    }
</style>>

</style>