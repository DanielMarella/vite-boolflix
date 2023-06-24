<template>
    <div class="container">
        <FindMovie @search=" searching "/>
    </div>
    <div class="container">
        <h1 class="text-danger mb-5">Lista dei film:</h1>
        <MovieList :movies="movies" />
        <h1 class="text-danger mb-5">Lista delle SerieTv:</h1>
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
                research : [],
                films : [],
                movies : [],
                movieApi : 'https://api.themoviedb.org/3/search/movie',
                filmsApi : 'https://api.themoviedb.org/3/search/tv',
            }
        },

        methods: {

            
            searching(text = '') {
                this.findMovie(text);
                this.findFilms(text);
                },

            

            findMovie(text = '') {
            axios.get(this.movieApi, {
                params: {
                query: text,
                api_key: '6e246ef7707d5632049a8350bf230c0f'
                }
            })
                .then((response) => {
                console.log(response);
                this.movies = response.data.results;
                })
                .catch(function (error) {
                console.log(error);
                });
            },

            findFilms(text = '') {
            axios.get(this.filmsApi, {
                params: {
                query: text,
                api_key: '6e246ef7707d5632049a8350bf230c0f',
                }
            })
                .then((response) => {
                console.log(response.data.results);
                this.films = response.data.results;
                })
                .catch(function (error) {
                console.log(error);
                });
            }
        },

    created() {
        this.searching();

    },

}
</script>

<style lang="scss" scoped>
    
</style>


