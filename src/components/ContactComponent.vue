<template>
    <div id="contact">
            <h1>contact</h1>
        <div v-for="(value,key) in object" v-bind:key="key">
            <a v-bind:href="value">{{key}}</a>
        </div>
    </div>
</template>

    <script>
export default{
    name: 'contact',
    data() {
        return{
            object:{
                github:"https://github.com/yamatcha",
                Twitter:"https://twitter.com/printf_yama",
                Instagram:"https://www.instagram.com/soju_yamacha/?hl=ja",
                Atcoder:"https://atcoder.jp/users/yamathca",
                Applemusic:"https://itunes.apple.com/profile/yamatcha",
            }
        }
    }
}
  </script>
<style>
#contact{
    font-size: 40px;
}
</style>
