<template>
  <div id="app">
    <Header></Header>
      <div id="button">
        <button @click="transpage('Home')" class="button">Home</button>
        <button @click="transpage('Info')" class="button">Info</button>
        <button @click="transpage('Language')" class="button">Language</button>
        <button @click="transpage('Contact')" class="button">Contact</button>
      </div>
      <transition name="fade">
      <component :is="currentPage"></component>
      </transition>
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
  data(){
    return{
      currentPage:'Home'
    }
  },
  components: {
    Header,
    Footer,
    Home,
    Info,
    Contact,
    Language
  },
  methods:{
    transpage(page){
      this.currentPage=page
    }
  }
}
</script>

<style>
#button{
  margin-top: 80px;
}
.button {
  display: inline-block;
  margin: 0 auto;
  width: 80pt;
  border: solid 1px silver;
  border-radius: 0.5rem 0.5rem;
  padding: 0.5rem 1.5rem;
  margin-top: 1rem;
  text-decoration: none;
}
.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
