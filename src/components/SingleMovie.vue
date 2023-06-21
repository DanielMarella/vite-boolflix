<template>

    <p>{{title}}</p>
    <p>{{ originalTitle }}</p>
    <p>{{ lang }}</p>
    <p>{{ rate }}</p>


</template>


<script>
    name : 'SingleMovie'
export default {
    props : {
        title : String,
        originalTitle : String,
        lang : String,
        rate : Number,
    }
}
</script>

<style lang="scss" scoped>
    
</style>