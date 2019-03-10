<template>
    <div id="content">
        <p id="titlei">
            Information
        </p>
        <div id="info">
            <div v-for="(value,key) in object" v-bind:key="key">
             {{key}}:{{value}}
            </div>
        </div>
    </div>
</template>

<script>
export default{
    name: 'info',
    data() {
        return{
            object:{
                Name: 'Yamatcha',
                Birthday: '1997/10/14',
                University: 'University of Electro Communications',
                Region: 'Tokyo',
                Major: 'Computer Science',
                Hobby: 'Music, Basketball, camera'
            }
        }
    }
}
 </script>
 <style>
 #titlei{
     font-size: 40px;
 }
 #info{
     font-size: 30px;
 }



 </style>
 
