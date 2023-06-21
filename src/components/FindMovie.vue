<template>
    <div class="container mb-5">

        <input type="text" v-model="searchMovie" >
        <button @click="$emit('search',searchMovie)"> Clicca qui per ricercare</button>

    </div>
</template>


<script>
    name : 'FindMovie'

    export default {
        searchMovie : '',
}

</script>

<style lang="scss" scoped>
    
</style>
