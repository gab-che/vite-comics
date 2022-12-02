<script>
    export default{
        data(){
            return{
                banner_items: [
                    {
                        img: 'buy-comics-digital-comics.png',
                        text: 'digital comics',
                    },{
                        img: 'buy-comics-merchandise.png',
                        text: 'dc merchandise',
                    },{
                        img: 'buy-comics-subscriptions.png',
                        text: 'subscription',
                    },{
                        img: 'buy-comics-shop-locator.png',
                        text: 'comic shop locator',
                    },{
                        img: 'buy-dc-power-visa.svg',
                        text: 'dc power visa',
                    }
                ]
            }
        },

        methods: {

        }
    }
</script>

<template>
    <section>
        <div class="container py-4 banner_container">
            <div class="banner_item d-flex"
            v-for="item, i in banner_items" :key="i + item.text">
                <div class="banner_img">
                    <img :src="`src/assets/img/${item.img}`" alt="{{item.text}}" class="img-fluid">
                </div>
                <div class="banner_text">
                    <span>{{item.text}}</span>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use '../styles/partials/variables' as *;

    section{
        background-color: $secondary_color;
    }

    .banner_container{
        @include flex_space_around;
    }

    .banner_item{
        align-items: center;
        gap: 1rem;
        .banner_img{
            width: 30px;
        }
    }
</style>