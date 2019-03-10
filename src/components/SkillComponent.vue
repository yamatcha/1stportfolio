<template>
  <div class="skill-wrapper">
    <h1>Skill</h1>
    <div class="contents-wrapper" id="skill-contentwrapper">
    <div class="skill-contents">
      <div v-for="(value,index) in vals" v-bind:key="index" class="skill-content">
        <skill-info v-bind="value"></skill-info> 
      </div>
    </div>
    </div>
   
  </div>
</template>

<script>
import SkillInfo from './SkillInfo.vue'
export default {
  name: 'app',
  components: {
    SkillInfo
  },
  data(){
    return{
      vals: [
        {name:"C", information:"大学入学してからずっと課題などで3年間ほど使っています。データ構造やアルゴリズムなどの勉強もCで行いました。一番使っている言語です。"},
        {name:"Java", information:"大学の授業で使いました。MVCデザインパターンの勉強を行いました。オブジェクト思考についてはある程度知識が入っています。"},
        {name:"Python", information:"C以外に使える軽量なスクリプト言語があると良いと思って勉強しました。udemyの講義を受けたり、みんなのpythonなどをやりました。個人的に好きな言語ですがあまり使い慣れていません、競技プログラミングをpyhtonで解いて練習しています。"},
        {name:"HTML/CSS", information:"デザインの素養がなく、あまり独学で勉強できていないので素人同然です。このサイトもフレームワークを使わずに自分でコーディングしました。"},
        {name:"Vue.js", information:"このサイトを作るにあたり、学習しました。即席で作ったため、深く理解できていませんが、ある程度の知識はついたかな、と思っています。"}
      ]
    }
  }
}
</script>

<style>
.skill-contentwrapper{
  display:flex;
  justify-content: center;
}
.skill-contents{
  margin-top :50px;
  margin-bottom:100px;
  display:flex;
  justify-content: space-between;
  align-content: space-between;
  align-self:stretch;
  flex-wrap:wrap;
}
</style>