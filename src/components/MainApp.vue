<template>
    <div>
        <FindMovie />
    </div>
    <div class="container mb-5">
        <h1>Lista dei film:</h1>
    </div>
    <div class="container">
        <MovieList :movies="movies" />
    </div>
</template>


<script>
import MovieList from './MovieList.vue';
import FindMovie from './FindMovie.vue';
import axios  from 'axios';


    name : 'MainApp'
export default {

    components : {
        MovieList,
        FindMovie,
    },
    
    data() {
            return {
                movies : [],
                apiUrl : 'https://api.themoviedb.org/3/discover/movie?api_key=6e246ef7707d5632049a8350bf230c0f',

            }
        },

        methods: {
            searchfilm(){
            axios.get(this.apiUrl)
            .then( (response) => {
                this.movies = response.data.results;
            })
            .catch(function (error) {
                console.log(error);
            })
        },
    },

    created() {
        this.searchfilm();
    },

}
</script>

<style lang="scss" scoped>
    
</style>