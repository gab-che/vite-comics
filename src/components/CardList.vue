<script>
    import SingleCard from './SingleCard.vue';
    export default{
        components: { SingleCard },

        props: {
            cards: Array
        },

        data(){
            return{
                
            }
        }
    }
</script>

<template>
    <div class="row">
        <div class="col-2" v-for="card in cards">
            <div class="card card_product">
                <img :src="card.thumb" class="card-img-top" :alt="card.series">
                <div class="card-body">
                    <h6 class="card-title">{{card.series}}</h6>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
    @use '../styles/partials/variables' as *;
    .card_product{
        background-color: transparent;

        .card-img-top{
            border-radius: 0;
        }
        .card-body{
            padding-inline: 0;
            text-transform: uppercase;
            font-size: .8rem;
        }
    }
</style>