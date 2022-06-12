<template>
  <main>
      <div class="container">
        <ul>
            <li v-for="movie in data.movies" :key="movie.id">
                <h3 class="title">{{movie.title}}</h3>
                <h4 class="original-title">{{movie.original_title}}</h4>
                <div class="vote">{{movie.vote_average}}</div>
                <div class="language">{{movie.original_title}}</div>
            </li>
        </ul>
      </div>
  </main>
</template>

<script>
import data from '../../shared/data'

export default {
    name: 'MainComponent',
    data(){
        return {
            data
        }
    }
}
</script>

<style lang="scss" scoped>
main {
    background-color: rgb(52, 52, 52);
    height: 100vh;
    overflow: auto;
}
</style>