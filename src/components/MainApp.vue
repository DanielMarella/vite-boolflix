<template>
    <div>
        <h3>Sono il MAIN</h3>
    </div>
    <MovieList />
</template>


<script>
import MovieList from './MovieList.vue';


    name : 'MainApp'
export default {

    components : {
        MovieList,
    }
    
}
</script>

<style lang="scss" scoped>
    
</style>