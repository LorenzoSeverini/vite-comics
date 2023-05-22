<!-- footer bottom -->
<script>
    export default {
        name : 'FooterBottom',

        data() {
            return {
                followUs : 'FOLLOW US',
                signUp : 'SIGN UP NOW!',

                FooterBottom: [
                    { image : '/public/vue-dc-comics-1/img/footer-facebook.png' }, 
                    { image : '/public/vue-dc-comics-1/img/footer-twitter.png' }, 
                    { image : '/public/vue-dc-comics-1/img/footer-youtube.png' }, 
                    { image : '/public/vue-dc-comics-1/img/footer-pinterest.png' }, 
                    { image : '/public/vue-dc-comics-1/img/footer-periscope.png' },
                ]
            }
        },

        methods : {
            //
        },

        computed : {
            //
        },
    }
</script>

<!-- template -->
<template>
    <!-- footer bottom -->
    <div class="footer-bottom">
        <div class="footer-bottom-container">
            <!-- button to sign up now -->
            <div class="footer-bottom-left">
                <button>{{ signUp }}</button>
            </div>
            <div class="footer-bottom-right">
                <h3>{{ followUs }}</h3>
                <!-- footer bottom images -->
                <div class="footer-bottom-container-item" v-for="(item, index) in FooterBottom" :key="index">
                    <img :src="item.image" alt="footer-bottom">
                </div>
            </div>
        </div>
    </div>
</template>

<!-- style css -->
<style scoped>

.footer-bottom {
    max-width: 75rem;
    margin: 0 auto;
    padding: 3rem 0;
}

.footer-bottom-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.footer-bottom-left {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 1rem;
}

.footer-bottom-left button {
    background-color: #303030;
    color: #fff;
    padding: 1rem;
    border: 1px solid #0282f9;
    font-size: 1rem;
    font-weight: 700;
    text-transform: uppercase;
    cursor: pointer;
}

.footer-bottom-left button:hover {
    background-color: #0282f9;
    color: #312f2f;
    /* transform: scale(1.1); */
}

.footer-bottom-left button:focus {
    outline: none;
}

.footer-bottom-right {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 1rem;
}

.footer-bottom-right h3 {
    color: #0282f9;
    font-size: 1.25rem;
    font-weight: 700;
    cursor: pointer;
}

.footer-bottom-container-item img {
    width: 1.5rem;
    height: 1.5rem;
    cursor: pointer;
}

.footer-bottom-container-item img:hover {
    opacity: 0.5;
}
</style>