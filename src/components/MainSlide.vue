<!-- slide like netflix img -->
<script>
    export default {
        name: 'MainSlide',
        data() {
            return {
                imageContainer : [
                    {
                        "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                        "price": "$19.99",
                        "series": "Action Comics",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                        "price": "$3.99",
                        "series": "American Vampire 1976",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                        "price": "$16.99",
                        "series": "Aquaman",
                        "type": "graphic novel",
                    },
                    {
                        "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                        "price": "$2.99",
                        "series": "Batgirl",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                        "price": "$3.99",
                        "series": "Batman",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                        "price": "$2.99",
                        "series": "Batman Beyond",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                        "price": "$3.99",
                        "series": "Batman/Superman",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                        "price": "$4.99",
                        "series": "Batman/Superman Annual",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                        "price": "$5.99",
                        "series": "Batman: The Joker War Zone",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                        "price": "$6.99",
                        "series": "Batman: Three Jokers",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                        "price": "$4.99",
                        "series": "Batman: White Knight Presents: Harley Quinn",
                        "type": "comic book",
                    },
                    {
                        "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                        "price": "$16.99",
                        "series": "Catwoman",
                        "type": "graphic novel",
                    },
                ],

                ButtonLoad : 'Load More',
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

    <!-- title currrent series -->
    <div class="title">
        <h2>Current Series</h2>
    </div>

    <!-- slide -->
    <div class="slide">
        <div class="slide-container">
            <div class="slide-container-item" v-for="(item, index) in imageContainer" :key="index">
                <img :src="item.thumb" :alt="item.series">
                <p>{{ item.price }}</p>
                <h3>{{ item.series }}</h3>
                <p>{{ item.type }}</p>
            </div>
        </div>
        <!-- Button to load more comics  -->
        <div class="slide-button">
            <button>{{ ButtonLoad }}</button>
        </div>
    </div>
    
</template>

<!-- style css -->
<style lang="scss" scoped>

.title {
    max-width: 75rem;
    margin: 0 auto;
    margin-bottom: 2rem;

    h2 {
        font-size: 1.5rem;
        font-weight: 700;
        text-transform: uppercase;
        color: brown;

        &:hover {
            cursor: pointer;
        }

        &::after {
            content: '';
            display: block;
            width: 3rem;
            height: 0.25rem;
            background-color: brown;
            margin-top: 0.5rem;
        }
    }
}

.slide {
    width: 100%;
    margin-bottom: 2rem;

    .slide-container {
        max-width: 75rem;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
        gap: 2rem;

        .slide-container-item {
            width: calc(100% / 6 - 2rem);
            display: flex;
            flex-direction: column;
            align-items: center;
            color: #fff;

            img {
                width: 100%;
                height: 12.5rem;
                margin-bottom: 1rem;
                cursor: pointer;
                object-fit: contain;
                object-position: center;

                &:hover {
                    opacity: 0.5;
                }
            }

            p {
                font-size: 0.75rem;
                font-weight: 700;
                text-align: center;
                color: brown;
                cursor: pointer;
            }

            h3 {
                font-size: 0.875rem;
                font-weight: 700;
                text-transform: uppercase;
                text-align: center;
                cursor: pointer;
            }
        }
    }

    .slide-button {
        display: flex;
        justify-content: center;
        align-items: center;
        margin-top: 2rem;

        button {
            background-color: #303030;
            color: #fff;
            padding: 1rem;
            border: 1px solid #0282f9;
            font-size: 1rem;
            font-weight: 700;
            text-transform: uppercase;
            cursor: pointer;

            &:hover {
                background-color: #0282f9;
                color: #312f2f;
            }
        }
    }
}

/* .title {
    max-width: 75rem;
    margin: 0 auto;
    margin-bottom: 2rem;
}

.title h2 {
    font-size: 1.5rem;
    font-weight: 700;
    text-transform: uppercase;
    color: brown;
}

.title h2:hover {
    cursor: pointer;
}

.title h2::after {
    content: '';
    display: block;
    width: 3rem;
    height: 0.25rem;
    background-color: brown;
    margin-top: 0.5rem;
}

.slide {
    width: 100%;
    margin-bottom: 2rem;
}

.slide-container {
    max-width: 75rem;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 2rem;
}

.slide-container-item {
    width: calc(100% / 6 - 2rem);
    display: flex;
    flex-direction: column;
    align-items: center;
    color: #fff;
}

.slide-container-item img {
    width: 100%;
    height: 12.5rem;
    margin-bottom: 1rem;
    cursor: pointer;
    object-fit: contain;
    object-position: center;

}

.slide-container-item img:hover {
    opacity: 0.5;
}

.slide-container-item p {
    font-size: 0.75rem;
    font-weight: 700;
    text-align: center;
    color: brown;
    cursor: pointer;
}

.slide-container-item h3 {
    font-size: 0.875rem;
    font-weight: 700;
    text-transform: uppercase;
    text-align: center;
    cursor: pointer;

}

.slide-button {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 2rem;
}

.slide-button button {
    background-color: #303030;
    color: #fff;
    padding: 1rem;
    border: 1px solid #0282f9;
    font-size: 1rem;
    font-weight: 700;
    text-transform: uppercase;
    cursor: pointer;
}

.slide-button button:hover {
    background-color: #0282f9;
    color: #312f2f;
} */
</style>