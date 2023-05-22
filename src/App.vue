<script>
  import HeaderNav from './components/HeaderNav.vue'
  import MainContent from './components/MainContent.vue'
  import MainSlide from './components/MainSlide.vue'
  import ShopComics from './components/ShopComics.vue'
  import FooterNav from './components/FooterNav.vue'
  import FooterBottom from './components/FooterBottom.vue'

  export default {
    name: 'App',
    components: {
      HeaderNav,
      MainContent,
      MainSlide,
      ShopComics,
      FooterNav,
      FooterBottom,
    },
    data () {
      return {
        //
      }
    },
    methods: {
      // 
    },
    computed: {
      // 
    },
  }
</script>

<!-- template -->
<template>

  <!-- header -->
  <header>
    <!-- header nav -->
    <HeaderNav />
  </header>

  <!-- main -->
  <main>
    <!-- main content -->
    <MainContent />
    <!-- Slide img -->
    <MainSlide />
    <!-- Shop content -->
    <ShopComics />
  </main>

  <!-- footer -->
  <footer>
    <!-- footer nav -->
    <FooterNav />

    <!-- footer bottom -->
    <FooterBottom />
  </footer>

</template>

<!-- style -->
<style scoped></style>
