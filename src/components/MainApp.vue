<template>
    <div>
        <h3>Sono il MAIN</h3>
    </div>
    <FindMovie />
    <MovieList />
</template>


<script>
import MovieList from './MovieList.vue';
import FindMovie from './FindMovie.vue';

    name : 'MainApp'
export default {

    components : {
        MovieList,
        FindMovie,
    }
    
}
</script>

<style lang="scss" scoped>
    
</style>