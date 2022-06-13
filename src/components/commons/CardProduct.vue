<template>
    <div class="card">
        <img :src="getUrl(info.poster_path)" alt="poster">
        <h3 class="title">{{info.title ? info.title : info.name}}</h3>
        <h4 class="original-title">{{info.original_title ? info.original_title : info.original_name}}</h4>
        <div class="vote">{{info.vote_average}}</div>
        <div class="language">{{info.original_lenguage}}</div>
    </div>
</template>

<script>
export default {
    name: 'CardProduct',
    props: {
        info: Object
    },
    methods: {
        getUrl(url) {
            return `http://image.tmdb.org/t/p/w185/${url}`
        }
    }
}
</script>

<style lang="scss" scoped>

</style>