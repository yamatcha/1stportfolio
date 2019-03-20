<template>
    <div id="contact-wrapper">
            <h1>contact</h1>
        <div class="contents-wrapper">
            <div v-for="(value,key) in object" v-bind:key="key" id="contact-content">
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
                Blog:"https://yamatcha.hatenablog.com/"
            }
        }
    }
}
  </script>
<style>
a{
    /* color:grey; */
    text-decoration: none;
    color:black;
    background-image: linear-gradient(to right, rgb(255, 255, 255) 50%, rgb(0, 0, 0) 50%);
    background-size:200% auto;
    transition:.3s;
}
a:hover{
    /* color:black; */
    background-position: -100% 0;
    color:white;
}
#contact-content{
    margin-top: 0.5rem;
}

</style>
