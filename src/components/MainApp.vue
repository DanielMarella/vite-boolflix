<template>
    <div>
        <FindMovie @search="searching"/>
    </div>
    <div class="container mb-5">
        <h1>Lista dei film:</h1>
    </div>
    <div class="container">
        <MovieList :movies="movies" />
        <SerieTvList :films="films" />
        
    </div>
</template>


<script>
import SerieTvList from './SerieTvList.vue';
import MovieList from './MovieList.vue';
import FindMovie from './FindMovie.vue';
import axios  from 'axios';


    name : 'MainApp'
export default {

    components : {
    MovieList,
    FindMovie,
    SerieTvList
},
    
    data() {
            return {
                films : [],
                movies : [],
                movieApi : 'https://api.themoviedb.org/3/search/movie',
                filmsApi : 'https://api.themoviedb.org/3/search/tv',
            }
        },

        methods: {
            searching(text = ''){
                axios.get(this.movieApi || this.filmsApi, {
                    params: {
                    query : text,
                    api_key : '6e246ef7707d5632049a8350bf230c0f',
                    }
                })
            .then( (response) => {
                console.log(response.data.results)
                this.movies = response.data.results;
                this.films = response.data.results;
                console.log(this.films)
            })
            .catch(function (error) {
                console.log(error);
            })
        },
    },

    created() {
        this.searching();
    },

}
</script>

<style lang="scss" scoped>
    
</style>


