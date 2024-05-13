<script>
import MyHeader from './components/MyHeader.vue';
import MyFooter from './components/MyFooter.vue';

export default {
    components: {
        MyHeader,
        MyFooter,
    },
    data() {
      return {
        
      }
    }
}

</script>

<template>
  <MyHeader />

  <router-view></router-view>
  
  <MyFooter />
</template>

<style  lang="scss">


</style>