<!-- main content -->
<script>
    export default {
        name: 'MainContent',
        data() {
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
    <div class="main-content">
        <div class="main-content-container">
            <div class="main-content-container-img">
                <img src="./public/vue-dc-comics-1/img/jumbotron.jpg" alt="jumbotron">
            </div>
        </div>
    </div>
</template>

<!-- style css -->
<style scoped>
.main-content {
    background-color: #151515;
    min-height: 31.25rem;
}

.main-content-container {
    margin: 0 auto;
    max-width: 75rem;
}

.main-content-container-img img {
    width: 100%;
    object-fit: cover;
    object-position: center;
}

.main-content-container-img img:hover {
    opacity: .8;
}

.main-content-container-img img:active {
    opacity: .5;
}

.main-content-container-img img:focus {
    opacity: .5;
}

.main-content-container-img img:visited {
    opacity: .5;
}

</style>