<template>
    <div class="container">
        <SingleMovie 
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
    components: {
        SingleMovie,
    },

    props : {
        movies : Array,  
    },
}
</script>

<style lang="scss" scoped>
    
</style>