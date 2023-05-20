<!-- Header Nav  -->
<script>
export default {
  name: 'HeaderNav',
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
  <div class="header-nav">
    <div class="header-nav-logo">
      <img src="//public/vue-dc-comics-1/img/dc-logo.png" alt="logo">
    </div>
    <div class="header-nav-menu">
      <ul>
        <li><a href="#"></a>Characters</li>
        <li><a href="#">Comics</a></li>
        <li><a href="#">Movies</a></li>
        <li><a href="#">Tv</a></li>
        <li><a href="#">Games</a></li>
        <li><a href="#">Collectibles</a></li>
        <li><a href="#">Videos</a></li>
        <li><a href="#">Fans</a></li>
        <li><a href="#">News</a></li>
        <li><a href="#">Shop</a></li>
      </ul>
    </div>
  </div>
</template>

<!-- style CSS -->
<style scoped>
.header-nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 0;
  margin: 0 auto;
  max-width: 1200px;
}

.header-nav-logo img {
  width: 100px;
}

.header-nav-menu ul {
  display: flex;
  justify-content: space-between;
  align-items: center;
  list-style: none;
}

.header-nav-menu ul li {
  margin: 0 10px;
}

.header-nav-menu ul li a {
  text-decoration: none;
  color: #313131;
  font-weight: bold;
}

.header-nav-menu ul li a:hover {
  color: #0c7cec;
}
</style>
