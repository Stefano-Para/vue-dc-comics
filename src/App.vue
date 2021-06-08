<template>
  <div id="app">

    <!-- header  -->
    <Header />
    
    <!-- main  -->
    <!-- <Cards /> -->
    <Main />

    <!-- footer  -->
    <Footer />

  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'
// import Cards from './components/Cards.vue'



export default { 
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
    // Cards
    }
}

</script>

<style lang="scss">
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
</style>
