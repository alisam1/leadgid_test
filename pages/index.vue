<template>
  <div id="page">
    <div class="container">
      <Header />
      <div id="content" class="site-content">
        <Carousel />
        <Card />
      </div>
    </div>
    <Footer />
  </div>
</template>
<script>
import Header from '~/components/Header.vue';
import Carousel from '~/components/Carousel.vue';
import Card from '~/components/Card.vue'
import Footer from '~/components/Footer.vue'
export default {
  components: { 
    Header,
    Card,
    Carousel,
    Footer
  },
  data() {
    return {
    }
  },
}
</script>
<style>
.container {
  margin: 0 20px;
  max-width: 100%;
}

.site-content {
  padding: 20px 0 40px;
}

@media (min-width:1090px) {
  .container {
    margin: 0 auto;
    width: 960px;
  }
}

/* Header */
.site-header {
  padding-top: 2em;
  padding-bottom: 1em;
}

.site-branding {
  margin-bottom: 1em;
  text-align: center;
}

.site-title {
  font: 60px/1 'Herr Von Muellerhoff', cursive;
  letter-spacing: 2px;
  margin-top: 25px;
  margin-bottom: 20px;
  text-align: center;
  text-transform: none;
}

.site-description {
  font: italic 300 14px 'Quattrocento Sans', sans-serif;
  margin-top: -15px;
  margin-bottom: 35px;
  padding-top: 0;
  letter-spacing: 0px;
  text-align: center;
  text-transform: none;
}

/* Menu */
.menu {
  display: table;
  margin: 0 auto;
}

.main-navigation {
  font: 700 14px 'Oswald', serif;
  background-color: #fff;
  letter-spacing: 1px;
  padding: 15px 0;
  border-top: 1px solid;
  border-bottom: 1px solid;
  text-transform: uppercase;
}

.main-navigation a {
  color: #222;
}

.main-navigation ul {
  list-style: none;
  margin: 0 auto;
  padding: 3px 0;
}

.main-navigation li {
  display: inline;
  float: left;
  margin: 0 1em;
  position: relative;
}

.menu-toggle {
  display: none;
}

@media screen and (max-width:1023px) {
  .menu-toggle {
    display: block;
  }

  .menu-toggle {
    background: none;
    border: 0;
    box-shadow: none;
    color: #ffffff;
    font-size: 14px;
    margin: 0 auto;
    outline-style: none;
    text-shadow: none;
    text-transform: uppercase;
    color: #222222;
    cursor: pointer;
  }

  .menu-toggle.--active ~ .menu {
    display: block;
  }

  .main-navigation {
    display: block;
    float: none;
    margin: 0 auto;
  }

  .main-navigation a {
    display: block;
    padding: 0.5em 0;
    text-decoration: none;
  }

  .main-navigation ul {
    display: none;
  }

  .main-navigation li {
    float: none;
    margin: 0;
    position: relative;
    padding: 0;
    text-align: center;
  }

  .main-navigation li:last-child {
    border-bottom: 0;
  }
}

/* Footer */
.site-footer {
  padding: 2em 0;
  text-align: center;
  background-color: #333;
  color: #999;
}

.site-footer a {
  text-decoration: none;
  color: #999;
}
</style>
