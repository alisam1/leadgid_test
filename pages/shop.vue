<template>
  <div id="page_shop">
    <div class="container">
        <Header />
        <div id="content_shop" class="site-content">
        <h1>Shop</h1>
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
  name: 'shop',
  data() {
    return {
    }
  },
}
</script>

<style lang="scss" scoped>
  #page_shop > .container
   {
     height: 90vh;
   }

  h1{
       color: #333333;
    }
</style>>

</style>