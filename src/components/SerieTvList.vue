<template>
    <div class="container d-flex flex-wrap">
        <SingleFilm v-for="films in films"
        :name = "films.name"
        :originalName = "films.original_name"
        :lang = "films.original_language"
        :rate = "films.vote_average"

        />
    </div>
</template>


<script>
import SingleFilm from './SingleFilm.vue';

    name : 'SerieTvList'

export default {

    data() {
        return {

        }
    },


    components: {
        SingleFilm,
    },

    props : {
        films : Array,  
    },
}
</script>

<style lang="scss" scoped>
    
</style>