<template>
  <div id="page_contact">
    <div class="container">
      <Header />
      <div id="content_contact" class="site-content">
       <h1>Contact</h1>
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
  name: 'contact',
  data() {
    return {
    }
  },
}
</script>

<style lang="scss" scoped>
  #page_contact > .container
   {
     height: 90vh;
   }

  h1{
      color: #333333;
    }
</style>>

</style>