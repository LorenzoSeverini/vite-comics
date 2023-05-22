<!-- Header Nav  -->
<script>
  export default {
    name: 'HeaderNav',
    data () {
      return {

      imageLogo : [
        {
          image: './public/vue-dc-comics-1/img/dc-logo.png',
          alt: 'logo',
        }
      ],

      menu: [
        {
          name: 'Characters',
          link: '#'
        },
        {
          name: 'Comics',
          link: '#'
        },
        {
          name: 'Movies',
          link: '#'
        },
        {
          name: 'Tv',
          link: '#'
        },
        {
          name: 'Games',
          link: '#'
        },
        {
          name: 'Collectibles',
          link: '#'
        },
        {
          name: 'Videos',
          link: '#'
        },
        {
          name: 'Fans',
          link: '#'
        },
        {
          name: 'News',
          link: '#'
        },
        {
          name: 'Shop',
          link: '#'
        },
      ]
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
      <img :src="imageLogo[0].image" :alt="imageLogo[0].alt">
    </div>
    <div class="header-nav-menu">
      <ul>
        <li v-for="(item, index) in menu" :key="index">
          <a :href="item.link">{{ item.name }}</a>
        </li>
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
  padding: 1rem 0;
  margin: 0 auto;
  max-width: 75rem;
}

.header-nav-logo img {
  width: 6.25rem;
  object-fit: cover;
  object-position: center;
  cursor: pointer;
}

.header-nav-menu ul {
  display: flex;
  justify-content: space-between;
  align-items: center;
  list-style: none;
}

.header-nav-menu ul li {
  margin: 0 .625rem;
}

.header-nav-menu ul li a {
  text-decoration: none;
  color: #313131;
  font-weight: bold;
}

.header-nav-menu ul li a:hover {
  color: #0c7cec;
  /* when is over show underline but at the bottom ov the nav bar */
  border-bottom: 2px solid #0c7cec;

}
</style>
