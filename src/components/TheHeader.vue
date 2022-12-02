<script>
    export default{
        data(){
            return{
                link_list: ["characters", "comics", "movies", "tv", "games", "collectibles", "videos", "fans", "news", "shop"],
            }
        },

        methods: {

        }
    }
</script>

<template>
    <header>
        <div class="container py-5">
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="" class="img-fluid">
            </div>

            <div class="navbar">
                <ul class="list-unstyled">
                    <li v-for="link in link_list"><a href="#">{{link}}</a></li>
                </ul>
            </div>
        </div>
    </header>
</template>

<style scoped lang="scss">
    @use '../styles/partials/variables' as *;
    
    .container{
        @include flex_space_between;

        ul{
            @include flex_space_between;
            gap: 1rem;
            text-transform: uppercase;
            margin-bottom: 0;
        }

        a{
            text-decoration: none;
            padding: .5rem;
            color: $primary_color;
        }
    }
    .logo{
        width: 50px;
    }

</style>