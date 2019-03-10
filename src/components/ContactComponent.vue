<template>
    <div id="contact-wrapper">
            <h1>contact</h1>
        <div class="content-wrapper">
            <div v-for="(value,key) in object" v-bind:key="key" id="contact">
                <a v-bind:href="value" target="_blank">{{key}}</a>
            </div>
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
a{
    color:grey;
    text-decoration: none;
}
a:hover{
    color:black;
}
#contact{
    margin-top: 0.5rem;
}
</style>
