<template>
  <div id="app">
    <Header></Header>
      <div id="button-wrapper">
        <button @click="transpage('Home')" class="button">Home</button>
        <button @click="transpage('Info')" class="button">Info</button>
        <button @click="transpage('Skill')" class="button">Skill</button>
        <button @click="transpage('Contact')" class="button">Contact</button>
      </div>
      <div id="main-content">
        <transition name="fade">
          <component :is="currentPage"></component>
        </transition>
      </div>
      <Footer></Footer>
  </div>
</template>

<script>
import Footer from './components/FooterComponent.vue'
import Header from './components/HeaderComponent.vue'
import Home from './components/HomeComponent.vue'
import Info from './components/InfoComponent.vue'
import Contact from './components/ContactComponent.vue'
import Skill from './components/SkillComponent.vue'


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
    Skill
  },
  methods:{
    transpage(page){
      this.currentPage=page
    }
  }
}
</script>

<style>
#button-wrapper{
  margin-top: 80px;
  display: flex;
}
.button {
  margin: 0 auto;
  width: 90pt;
  padding: 0.5rem 1.5rem;
  margin-top: 1rem;
  background: #fff;
  color : #000;
  border: solid 4px #000;
  border-radius: 3px;
  transition: .4s;
  font-weight: bold;
}
.button:hover {
  background: #000;
  color: white;
}
.fade-enter-active{
  transition: all 1.2s ease-in;
}
.fade-leave-active{
  transition: all .4s ease-in;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
  transform: translateX(10px);
}

#main-content{
  margin-top : 1.5rem;
  margin-left: 3rem;
  padding-bottom: 60px;
}

body{
  /* font-family: 'Helvetica'; */
  font-family: 'Lato', 'Noto Sans JP', '游ゴシック Medium', '游ゴシック体', 'Yu Gothic Medium', YuGothic, 'ヒラギノ角ゴ ProN', 'Hiragino Kaku Gothic ProN', 'メイリオ', Meiryo, 'ＭＳ Ｐゴシック', 'MS PGothic', sans-serif;
}

h1{
  display:flex;
  justify-content: center;
}

.contents-wrapper{
     font-size: 30px;
     margin-top: 2.5rem;
 }


 /*resopnsive design */
 @media screen and (max-width:639px) {
/*スマホ用のcssを記述*/
#main-content{
  margin-left: 1rem;
  margin-top: 0.8rem
}
.contents-wrapper{
  font-size: 18px;
  margin-top:1.0rem;
}

}
</style>
