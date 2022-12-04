<script>
    export default{
        data(){
            return{
                icons: [
                'footer-facebook.png',
                'footer-periscope.png',
                'footer-pinterest.png',
                'footer-twitter.png',
                'footer-youtube.png'
                ]
            }
        },

        methods: {

        }
    }
</script>

<template>
    <footer>
        <div class="container sec_footer">
            <div class="sign_up">
                <button class="btn btn_sign">SIGN UP NOW!</button>
            </div>
            <div class="follow_container d-flex align-items-center gap-3">
                <span>FOLLOW US</span>
                <ul class="icon_list list-unstyled mb-0 d-flex gap-3">
                    <li v-for="icon in icons">
                        <a href="#"><img :src="`src/assets/img/${icon}`" alt=""></a>
                    </li>
                </ul>
            </div>
        </div>
    </footer>
</template>

<style scoped lang="scss">
    @use '../styles/partials/variables' as *;

    footer{
        @include z_index_up;
        background-color: $footer_color;
        padding: 3rem 0;
    };

    .sec_footer{
        @include flex_space_between;
    }

    .btn_sign{
        color: $accent_color_light;
        font-weight: 600;
        border: 2px solid $secondary_color;
        border-radius: 0;
    }

    .follow_container{
        span{
            color: $secondary_color;
            font-weight: 600;
        }
    }
</style>