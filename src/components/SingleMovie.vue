<template>
<div class="card mx-3 mb-3">

    <p>Titolo: {{title}}</p>
    <p>Titolo Originale: {{ originalTitle }}</p>
    <p>Lingua: {{ lang }}</p>
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
        height: 200px ;
        border: 2px solid black;
    }
</style>