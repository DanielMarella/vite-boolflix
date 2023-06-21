<template>
    <div>
        <FindMovie @search="searchMovies"/>
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
                apiUrl : 'https://api.themoviedb.org/3/search/movie?',
                
            }
        },

        methods: {
            searchMovies(text = ''){
                axios.get(this.apiUrl, {
                    params: {
                    query : text,
                    api_key : '6e246ef7707d5632049a8350bf230c0f',
                    }
                })
            .then( (response) => {
                this.movies = response.data.results;
                console.log(this.movies)
            })
            .catch(function (error) {
                console.log(error);
            })
        },


    },

    created() {
        this.searchMovies();
    },

}
</script>

<style lang="scss" scoped>
    
</style>


