<template>
  <main>
      <div class="container">
        <div class="movies-box">
            <h2>Movies</h2>
            <ul>
                <li v-for="movie in data.movies" :key="movie.id">
                    <CardProduct :info="movie"/>
                </li>
            </ul>
        </div>
        <div class="series-box">
            <h2>Series</h2>
            <ul>
                <li v-for="series in data.tv" :key="series.id">
                    <CardProduct :info="series"/>
                </li>
            </ul>
            </div>
      </div>
  </main>
</template>

<script>
import data from '../../shared/data'
import CardProduct from '../commons/CardProduct.vue'

export default {
    components: {
        CardProduct
    },
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