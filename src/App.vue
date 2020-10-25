<template>
  <div id="app">
    <Header/>
    <Banner/>
    <Popular/>
    <Footer/>
  </div>
</template>

<script>
import Banner from './components/Banner.vue'
import Footer from './components/Footer.vue'
import Header from './components/Header.vue'
import Popular from './components/Popular.vue'

export default {
  name: 'App',
  components: {
    Banner,
    Footer,
    Header,
    Popular
  }
}
</script>
