<template>
    <div class="container d-flex flex-wrap">
        <SingleMovie v-for="movies in movies"
        :title = "movies.title"
        :originalTitle = "movies.original_title"
        :lang = "movies.original_language"
        :rate = "movies.vote_average"

        />
    </div>
</template>


<script>
import SingleMovie from './SingleMovie.vue';

    name : 'MovieList'

export default {

    data() {
        return {

        }
    },


    components: {
        SingleMovie,
    },

    props : {
        movies : Object,  
    },
}
</script>

<style lang="scss" scoped>
    
</style>