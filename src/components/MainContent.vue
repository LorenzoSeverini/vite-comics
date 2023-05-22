<!-- main content -->
<script>
    export default {
        name: 'MainContent',
        data() {
            return {
                Jumbotron: [
                    {
                        image: './public/vue-dc-comics-1/img/jumbotron.jpg',
                        alt: 'jumbotron',
                    }
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
    <div class="main-content">
        <div class="main-content-container">
            <div class="main-content-container-img">
                <img :src="Jumbotron[0].image" :alt="Jumbotron[0].alt">
            </div>
        </div>
    </div>
</template>

<!-- style -->
<style lang="scss" scoped>

.main-content {
    width: 100%;
    height: 100%;
    padding: 2rem;

    .main-content-container {
        width: 100%;
        height: 100%;
        max-width: 1200px;
        margin: 0 auto;

        .main-content-container-img img {
            width: 100%;
            height: auto;
            border-radius: 0.5rem;
            transition: 0.3s;
            object-fit: contain;
            object-position: center;
            aspect-ratio: 16/9;
        }
    }
}


/* .main-content {
    width: 100%;
    height: 100%;
    padding: 2rem;
}

.main-content-container {
    width: 100%;
    height: 100%;
    max-width: 1200px;
    margin: 0 auto;
}
.main-content-container-img img {
    width: 100%;
    height: auto;
    border-radius: 0.5rem;
    transition: 0.3s;
    object-fit: contain;
    object-position: center;
    aspect-ratio: 16/9;
} */
</style>