<template>
  <header>
    <div class="container">
        <div class="logo">
            <a href="#"><img src="/img/logo-netflix.png" alt=""></a>
        </div>
        <div class="searchbar">
            <form>
                <input type="text" placeholder="Search movie">
                <button type="submit">Search</button>
            </form>
        </div>
    </div>
  </header>
</template>

<script>
export default {
    name: 'HeaderComponent'
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