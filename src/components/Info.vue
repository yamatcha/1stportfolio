<template>
    <div id="Info">
        <div v-for="(value,key) in object" v-bind:key="key">
           {{key}}:{{value}}
        </div>
    </div>
</template>

<script>
export default{
    name: 'Info',
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
