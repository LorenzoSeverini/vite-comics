<!-- Shop -->
<script>
    export default {
        name: 'ShopComics',
        data () {
        return {

            Marchandise: [
                {
                    image: './public/vue-dc-comics-1/img/buy-comics-digital-comics.png',
                    name: 'DC Shop',
                    link: '#'
                },
                {
                    image: './public/vue-dc-comics-1/img/buy-comics-merchandise.png',
                    name: 'DC Power Visa',
                    link: '#'
                },
                {   
                    image: './public/vue-dc-comics-1/img/buy-comics-subscriptions.png',
                    name: 'Additional DC Sites',
                    link: '#'
                },
                {
                    image: './public/vue-dc-comics-1/img/buy-comics-shop-locator.png',
                    name: 'Shop Locations',
                    link: '#'
                },
                {
                    image: './public/vue-dc-comics-1/img/buy-dc-power-visa.svg',
                    name: 'DC Power Visa',
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
    <!-- marchandise -->
    <div class="shop-comics">
        <div class="shop-comics-container">
            <div class="shop-comics-container-item" v-for="(item, index) in Marchandise" :key="index">
                <img :src="item.image" :alt="item.name">
                <a :href="item.link">{{ item.name }}</a>
            </div>
        </div>
    </div>

</template>

<!-- Style -->
<style lang="scss" scoped>

.shop-comics {
    background-color: #0282f9;
    padding: 1.25rem 0;

    .shop-comics-container {
        max-width: 1200px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;

        .shop-comics-container-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            color: #fff;

            img {
                width: 6.25rem;
                height: 7.5rem;
                margin-bottom: 0.625rem;
                cursor: pointer;

                &:hover {
                    opacity: 0.5;
                }
            }

            a {
                font-size: 0.75rem;
                text-transform: uppercase;
                font-weight: 700;
                letter-spacing: 0.1rem;
                text-decoration: none;
                color: #fff;
                cursor: pointer;

                &:hover {
                    text-decoration: underline;
                }
            }
        }
    }
}

/* .shop-comics {
    background-color: #0282f9;
    padding: 1.25rem 0;
}

.shop-comics-container {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.shop-comics-container-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    color: #fff;
}

.shop-comics-container-item img {
    width: 6.25rem;
    height: 7.5rem;
    margin-bottom: 0.625rem;
    cursor: pointer;
}

.shop-comics-container-item img:hover {
    opacity: 0.5;
}

.shop-comics-container-item a {
    font-size: 0.75rem;
    text-transform: uppercase;
    font-weight: 700;
    letter-spacing: 0.1rem;
    text-decoration: none;
    color: #fff;
    cursor: pointer;
}

.shop-comics-container-item a:hover {
    text-decoration: underline;
} */
</style>