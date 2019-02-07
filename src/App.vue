<template>
  <div id="app">
    <Header></Header>
    <Home></Home>
    <Info></Info>
    <Contact></Contact>
    <Language></Language>
    <Footer></Footer>
  </div>
</template>

<script>
import Footer from './components/Footer.vue'
import Header from './components/Header.vue'
import Home from './components/Home.vue'
import Info from './components/Info.vue'
import Contact from './components/Contact.vue'
import Language from './components/Language.vue'


export default {
  name: 'app',
  components: {
    Header,
    Footer,
    Home,
    Info,
    Contact,
    Language
  }
}
</script>

<style>

</style>
