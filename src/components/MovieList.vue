<template>

    <h4>
        sono la movie list
    </h4>
    <SingleMovie />
</template>


<script>
import SingleMovie from './SingleMovie.vue';

    name : 'MovieList'

export default {
    components: {
        SingleMovie,
    }
}
</script>

<style lang="scss" scoped>
    
</style>