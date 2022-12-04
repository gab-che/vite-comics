<script>
import { helperNameMap } from '@vue/compiler-core';

    export default{
        data(){
            return{
                footer_links: [
                    {
                        list_title: 'dc comics',
                        list_links: ['charachters', 'comics', 'movies', 'tv', 'games', 'videos', 'news']
                    },
                    {
                        list_title: 'shop',
                        list_links: ['shop DC', 'shop DC collectibles']
                    },
                    {
                        list_title: 'dc',
                        list_links: ['terms of use', 'privacy policy (New)', 'ad choices', 'advertising', 'jobs', 'subscriptions', 'talent workshops', 'CPSC certificates', 'ratings', 'shop help', 'contact us']
                    },
                    {
                        list_title: 'sites',
                        list_links: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
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
        <div class="container">
            <div class="row">
                <div class="col-6">
                    <div class="row-cols-3 d-flex gap-3">
                        <div class="col">
                            <div class="footer_title text-uppercase">
                                <h5>{{footer_links[0].list_title}}</h5>
                            </div>
                            <ul class="footer_links list-unstyled">
                                <li v-for="link in footer_links[0].list_links">
                                    <a href="#">{{link}}</a>
                                </li>
                            </ul>
                            <div class="footer_title text-uppercase">
                                <h5>{{footer_links[1].list_title}}</h5>
                            </div>
                            <ul class="footer_links list-unstyled">
                                <li v-for="link in footer_links[1].list_links">
                                    <a href="#">{{link}}</a>
                                </li>
                            </ul>
                        </div>
                        <div class="col">
                            <div class="footer_title text-uppercase">
                                <h5>{{footer_links[2].list_title}}</h5>
                            </div>
                            <ul class="footer_links list-unstyled">
                                <li v-for="link in footer_links[2].list_links">
                                    <a href="#">{{link}}</a>
                                </li>
                            </ul>
                        </div>
                        <div class="col">
                            <div class="footer_title text-uppercase">
                                <h5>{{footer_links[3].list_title}}</h5>
                            </div>
                            <ul class="footer_links list-unstyled">
                                <li v-for="link in footer_links[3].list_links">
                                    <a href="#">{{link}}</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="col-6 d-flex justify-content-end">
                    <div class="big_logo">
                        <img src="../assets/img/dc-logo-bg.png" alt="" class="img-fluid">
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
    @use '../styles/partials/variables' as *;
    
    section{
        background-image: url('../assets/img/footer-bg.jpg');
        background-repeat: no-repeat;
        padding: 3rem 0;
        position: relative;
    }

    .big_logo{
        width: 500px;
        position: absolute;
        top: -10%;
    }
    
    .footer_title{
        color: $accent_color_light;
    }

    .footer_links{
        a{
            color: $accent_color_dark;
            text-decoration: none;
            font-size: .8rem;
        }
    }

</style>