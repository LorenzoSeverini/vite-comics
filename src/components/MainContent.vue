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

<!-- style css -->
<style scoped>
.main-content-container-img img {
    width: 100%;
    height: auto;
}

.main-content-container-img img:hover {
    opacity: 0.8;
}
</style>