<template>
<div class="card mx-3 mb-3">
    <h3>Movie</h3>
    <p><img :src="`${imageUrl}${imageSize}${img}`"></p>
    <p>Titolo: {{title}}</p>
    <p>Titolo Originale: {{ originalTitle }}</p>
    <p v-if="langToCheck.includes(lang)">Lingua: {{ lang.toUpperCase() }}</p>
    <p v-else><img  :src="`https://www.countryflagicons.com/FLAT/32/${lang.toUpperCase()}.png`"></p>
    <p>
        Voto: {{ interRate() }}   
    </p>
    <div class="star d-flex">
            <p v-for="star in 5">
                <font-awesome-icon v-if="rate >= star *2" icon="fa-solid fa-star"/>
                <font-awesome-icon v-else icon="fa-regular fa-star" />
            </p>
        </div>
    
</div>


</template>


<script>
    name : 'SingleMovie'
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
        title : String,
        originalTitle : String,
        lang : String,
        rate : Number,
    },

    methods: {
        interRate(){
            return Math.ceil(this.rate / 2 ).toFixed(0);
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