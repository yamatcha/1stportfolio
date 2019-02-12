<template>
  <div id="app">
    <Header></Header>
      <div id="button">
        <button @click="transpage('Home')" class="button">Home</button>
        <button @click="transpage('Info')" class="button">Info</button>
        <button @click="transpage('Language')" class="button">Language</button>
        <button @click="transpage('Contact')" class="button">Contact</button>
      </div>
      <div id="main">
        <transition name="fade">
          <component :is="currentPage"></component>
        </transition>
      </div>
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
  display: flex;
}
.button {
  margin: 0 auto;
  width: 90pt;
  padding: 0.5rem 1.5rem;
  margin-top: 1rem;
  text-decoration: none;
  background: #fff;
  color : #67c5ff;
  border: double 4px #67c5ff;
  border-radius: 3px;
  transition: .4s;
  font-weight: bold;
}
.button:hover {
  background: #67c5ff;
  color: white;
}
.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
  transition: opacity .4s;
}

#main{
  display: flex;
  justify-content: center;
}

body{
  font-family: 'Libre Barcode 39 Text', cursive;
}
</style>
