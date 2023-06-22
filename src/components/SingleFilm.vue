<template>
    <div class="card mx-3 mb-3">
        <h3>Tv Series</h3>
        <p>Nome: {{name}}</p>
        <p>Nome Originale: {{ originalName }}</p>
        <p>Lingua:<img :src="`https://www.countryflagicons.com/FLAT/32/${lang.toUpperCase()}.png`"></p>
        <p>Voto: {{ rate }}</p>
    </div>
    
    
    </template>
    
    
    <script>
        name : 'SingleFilm'
    export default {
        props : {
            name : String,
            originalName : String,
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