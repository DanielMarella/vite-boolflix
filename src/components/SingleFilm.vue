<template>
    <div class="card mx-3 mb-3">
        <h3>Tv Series</h3>
        <p>Nome: {{name}}</p>
        <p>Nome Originale: {{ originalName }}</p>
        <p v-if="langToCheck.includes(lang)">Lingua: {{ lang.toUpperCase() }}</p>
        <p v-else><img  :src="`https://www.countryflagicons.com/FLAT/32/${lang.toUpperCase()}.png`"></p>
        <p>Voto: {{ rate }}</p>
    </div>
    
    
    </template>
    
    
    <script>
        name : 'SingleFilm'
    export default {

        data() {
            return {
                langToCheck : ['en','ja','hi','da','zh','iu'],
            }
        },

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