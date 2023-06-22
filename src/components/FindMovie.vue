<template>
    <div class="container mb-5">

        <input type="text" v-model="searchText" >
        <button @click="$emit('search',searchText)"> Clicca qui per ricercare</button>

    </div>
</template>


<script>
    name : 'FindMovie'

    export default {
        searchText : '',
}

</script>

<style lang="scss" scoped>
    
</style>
