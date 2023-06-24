<template>

    <div class="card mx-2 mb-4" style="width: 18rem;">
        <img :src="`${imageUrl}${imageSize}${img}`">
        <div class="card-body">
            <h5 class="card-title">Titolo: <br>{{title}}</h5>
            <h5 class="card-title">Titolo Originale: <br>{{ originalTitle }}</h5>
            <hr>
            <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
        </div>
        <ul class="list-group list-group-flush">
            <li class="list-group-item" v-if="langToCheck.includes(lang)"> Lingua: <strong>{{ lang.toUpperCase() }}</strong></li>
            <li class="list-group-item" v-else> Lingua: <img  :src="`https://www.countryflagicons.com/FLAT/32/${lang.toUpperCase()}.png`"></li>
            <li class="list-group-item"> Voto: {{ interRate() }}</li>
            <li class="list-group-item star d-flex">
                <p v-for="star in 5">
                    <font-awesome-icon v-if="rate >= star *2" icon="fa-solid fa-star" style="color: #ffff00;" />
                    <font-awesome-icon v-else icon="fa-regular fa-star" style="color: #ffff00;"  />
                </p>
            </li>
        </ul>
    </div>
</template>

<script>
    name : 'SingleMovie'
export default {

    data() {
        return {
            langToCheck : ['en','ja','hi','da','zh','iu'],
            imageUrl: 'https://image.tmdb.org/t/p/',
            imageSize : 'w342',
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
        color: white;
        width: 200px ;
        border: 2px solid red;

        .card-body,
        .list-group-item{
            color: white;
            border-color: red;
            background-color: #0f0f0f;
        }
    }
</style>