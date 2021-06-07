<template>
  <div id="app">

    <!-- header  -->
    <Header/>
    <header>Header page</header>

    <!-- main  -->
    <main>Main page</main>
    <!-- footer  -->
    <footer>Footer page</footer>

  </div>
</template>

<script>
import Header from './components/Header.vue'

export default { 
  name: 'App',
  components: {
    Header
  }
}

</script>

<style lang="scss">

</style>
