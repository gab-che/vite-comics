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
        <div class="container py-4">
            <ul class="banner_container list-unstyled">
                <li class="d-flex"
                v-for="item, i in banner_items" :key="i + item.text">
                    <a href="#" class="banner_item d-flex">
                        <div class="banner_img">
                            <img :src="`src/assets/img/${item.img}`" alt="{{item.text}}" class="img-fluid">
                        </div>
                        <div class="banner_text">
                            <span>{{item.text}}</span>
                        </div>
                    </a>
                </li>
            </ul>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use '../styles/partials/variables' as *;

    section{
        @include z_index_up;
        background-color: $secondary_color;
    }

    .banner_container{
        @include flex_space_around;
        margin-bottom: 0;
    }

    .banner_item{
        align-items: center;
        gap: 1rem;
        text-transform: uppercase;
        font-size: .8rem;
        color: $accent_color_light; 
        .banner_img{
            width: 30px;
        }
    }

    a{
        text-decoration: none;
        padding: .5rem;
    }
</style>