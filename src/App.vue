<script>
  import TheHeader from './components/TheHeader.vue';
  import MainContent from './components/MainContent.vue';
  import TheBanner from './components/TheBanner.vue';
  import MainFooter from './components/MainFooter.vue';
  import SecondaryFooter from './components/SecondaryFooter.vue';

  export default{
    components: { TheHeader, MainContent, TheBanner, MainFooter, SecondaryFooter },

    data(){
      return{

      }
    },

    methods:{

    }
  }
</script>

<template>
  <TheHeader></TheHeader>
  <MainContent></MainContent>
</template>

<style lang="scss">
	@use './styles/general.scss';
</style>
