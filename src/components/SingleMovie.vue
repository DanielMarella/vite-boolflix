<template>
<div class="card mx-3 mb-3">
    <h3>Movie</h3>
    <p>Titolo: {{title}}</p>
    <p>Titolo Originale: {{ originalTitle }}</p>
    <p>Lingua: 

        <img :src="`https://www.countryflagicons.com/FLAT/32/${lang.toUpperCase()}.png`">

</p>
    <p>Voto: {{ rate }}</p>
</div>


</template>


<script>
    name : 'SingleMovie'
export default {


    props : {
        title : String,
        originalTitle : String,
        lang : String,
        rate : Number,
    }
}
</script>

<style lang="scss" scoped>
    .card{
        width: 200px ;
        height: 250px ;
        border: 2px solid black;
    }
</style>