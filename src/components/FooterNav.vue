<!-- Footer Nav -->
<script>
    export default {
        name: 'FooterNav',

        data() {
            return {

                FooterNav: [

                    {
                        name: 'DC Comics',
                        link: '#',
                        subMenu: [
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
                                name: 'TV',
                                link: '#'
                            },
                            {
                                name: 'Games',
                                link: '#'
                            },
                            {
                                name: 'Videos',
                                link: '#'
                            },
                            {
                                name: 'News',
                                link: '#'
                            }
                        ],
                    },
                    {
                        name: 'Shop',
                        link: '#',
                        subMenu: [
                            {
                                name: 'Shop DC',
                                link: '#'
                            },
                            {
                                name: 'Shop DC Collectibles',
                                link: '#'
                            }
                        ]
                    },
                    {
                        name: 'DC',
                        link: '#',
                        subMenu: [
                            {
                                name: 'Terms Of Use',
                                link: '#'
                            },
                            {
                                name: 'Privacy policy (New)',
                                link: '#'
                            },
                            {
                                name: 'Ad Choices',
                                link: '#'
                            },
                            {
                                name: 'Advertising',
                                link: '#'
                            },
                            {
                                name: 'Jobs',
                                link: '#'
                            },
                            {
                                name: 'Subscriptions',
                                link: '#'
                            },
                            {
                                name: 'Talent Workshops',
                                link: '#'
                            },
                            {
                                name: 'CPSC Certificates',
                                link: '#'
                            },
                            {
                                name: 'Ratings',
                                link: '#'
                            },
                            {
                                name: 'Shop Help',
                                link: '#'
                            },
                            {
                                name: 'Contact Us',
                                link: '#'
                            }
                        ]
                    },
                    {
                        name: 'Sites',
                        link: '#',
                        subMenu: [
                            {
                                name: 'DC',
                                link: '#'
                            },
                            {
                                name: 'MAD Magazine',
                                link: '#'
                            },
                            {
                                name: 'DC Kids',
                                link: '#'
                            },
                            {
                                name: 'DC Universe',
                                link: '#'
                            },
                            {
                                name: 'DC Power Visa',
                                link: '#'
                            }
                        ]
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
    <!-- footer nav -->
    <div class="footer-nav">
        <div class="footer-nav-container">
            <!-- left -->
            <div class="footer-nav-left">
                <div class="footer-nav-container-item" v-for="(item, index) in FooterNav" :key="index">
                    <h3>{{ item.name }}</h3>
                    <ul>
                        <li v-for="(subItem, index) in item.subMenu" :key="index">
                            <a :href="subItem.link">{{ subItem.name }}</a>
                        </li>
                    </ul>
                </div>
            </div>
            <!-- right -->
            <div class="footer-nav-right">
                <div class="footer-logo-bg"></div>
            </div>
        </div>
    </div>
</template>

<!-- style css -->
<style scoped>

.footer-nav {
    background-image: url('./public/vue-dc-comics-1/img/footer-bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    min-height: 31.25rem;
}

.footer-nav-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 75rem;
    margin: 0 auto;
}

.footer-nav-left {
    display: flex;
    justify-content:flex-start;;
    width: 40%;
    gap: 2rem;
    padding-top: 1.25rem;
}

.footer-nav-left h3 {
    color: #fff;
    font-size: 1.25rem;
    font-weight: 700;
    cursor: pointer;
}

.footer-nav-left ul {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    padding-top: 0.5rem;
}

.footer-nav-left ul li {
    list-style: none;
}

.footer-nav-left ul li a {
    color: #9c9999;
    font-size: 0.875rem;
    font-weight: 400;
    cursor: pointer;
    text-decoration: none;
}

.footer-nav-left ul li a:hover {
    color: #fff;
}

.footer-nav-right {
    width: 40%;
}

.footer-logo-bg {
    background-image: url('./public/vue-dc-comics-1/img/dc-logo-bg.png');
    background-repeat: no-repeat;
    background-size: contain;
    background-position: center;
    height: 37.5rem
}
</style>  