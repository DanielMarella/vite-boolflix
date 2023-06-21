<template>
    <div>
        <FindMovie />
    </div>
    <div class="container mb-5">
        <h1>Lista dei film:</h1>
    </div>
        <MovieList :movies="movies" />
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
            }
        },

        methods: {
            searchfilm(){
            axios.get('https://api.themoviedb.org/3/movie/550?api_key=6e246ef7707d5632049a8350bf230c0f')
            .then( (response) => {
                this.movies = response.data;
                console.log(this.movies);
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