<template>
<div id="skill-info">
        <h3>{{name}}</h3>
    <div id="content-skill">
        <p>{{information}}</p>
    </div>
</div>
</template>

<script>
export default{
    props:{
        name:String,
        information:String
    }
}
</script>
<style>
#skill-info{
    border-top:solid 3px black;
}
</style>