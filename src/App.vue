<script>
  import HeaderNav from './components/HeaderNav.vue'
  import MainContent from './components/MainContent.vue'

  export default {
    name: 'App',
    components: {
      HeaderNav,
      MainContent,
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
  </main>
</template>

<style scoped></style>
