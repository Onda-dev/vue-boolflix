<template>
  <header>
    <div class="container">
        <div class="logo">
            <a href="#"><img src="/img/logo-netflix.png" alt=""></a>
        </div>
        <div class="searchbar">
            <form @submit.prevent="searching">
                <input type="text" placeholder="Search movie" v-model="searchText" required>
                <button type="submit">Search</button>
            </form>
        </div>
    </div>
  </header>
</template>

<script>
import axios from 'axios'
import data from '../../shared/data'

export default {
    name: 'HeaderComponent',
    data() {
        return {
            data,
            searchText: ''
        }
    },
    methods: {
        searching() {
            axios.get('https://api.themoviedb.org/3/search/movie', {
                params: {
                    api_key: 'bd410fbd725b090b8198430bb389db24',
                    query: this.searchText,
                    language: 'it, IT'
                }
            }).then((response) => {
                data.movies = response.data.results
            }).catch((error) => {
                console.log(error)
            })
        }
    }
}
</script>

<style lang="scss" scoped>
header {
    background-color: black;
    .container {
        padding: 1rem;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
}
.logo {
    width: 10%;
    img {
        width: 100%;
        display: block;
    }
}
</style>