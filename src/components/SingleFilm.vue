<template>
    <div class="card mx-3 mb-3">
        <h3>Tv Series</h3>
        <p><img :src="`${imageUrl}${imageSize}${img}`"></p>
        <p>Nome: {{name}}</p>
        <p>Nome Originale: {{ originalName }}</p>
        <p v-if="langToCheck.includes(lang)">Lingua: {{ lang.toUpperCase() }}</p>
        <p v-else><img  :src="`https://www.countryflagicons.com/FLAT/32/${lang.toUpperCase()}.png`"></p>
        <p>
        Voto: 
        {{ interRate() }}   
        
        <font-awesome-icon v-if="rate >= 2" icon="fa-solid fa-star"/>
        <font-awesome-icon v-else="rate <= 2" icon="fa-regular fa-star" />

        <font-awesome-icon v-if="rate >= 4" icon="fa-solid fa-star"/>
        <font-awesome-icon v-else="rate <= 4" icon="fa-regular fa-star" />

        <font-awesome-icon v-if="rate >= 6" icon="fa-solid fa-star"/>
        <font-awesome-icon v-else="rate <= 6" icon="fa-regular fa-star" />

        <font-awesome-icon v-if="rate >= 8" icon="fa-solid fa-star"/>
        <font-awesome-icon v-else="rate <= 8" icon="fa-regular fa-star" />

        <font-awesome-icon v-if="rate >= 10" icon="fa-solid fa-star"/>
        <font-awesome-icon v-else="rate <= 10" icon="fa-regular fa-star" />
    </p>
    </div>
    
    <i class="fa-solid fa-star"></i>
    </template>
    
    
    <script>
        name : 'SingleFilm'
    export default {

        data() {
            return {
                langToCheck : ['en','ja','hi','da','zh','iu'],
                imageUrl: 'https://image.tmdb.org/t/p/',
                imageSize : 'w154',
            }
        },

        props : {
            img : Image,
            name : String,
            originalName : String,
            lang : String,
            rate : Number,
        },

        methods: {
        interRate(){
            return Math.round(this.rate / 2 ).toFixed(0);
        }
    },

    }
    </script>
    
    <style lang="scss" scoped>
        .card{
            width: 200px ;
            border: 2px solid black;
        }
    </style>