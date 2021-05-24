<template>
  <div id="app">
    <div class="container">
      <h1 class="text-center mt-5">Vue Dischi</h1>
      <div class="row">
        <Disc
          v-for="(disc, index) in discs"
          :key= 'index'
          :disc='disc'
         />
        

      </div>
    </div>
  </div>
</template>

<script>

import axios from 'axios';
import Disc from '@/components/Disc.vue';

export default {
  name: "App",
  components: {
    Disc,
    
  },
  data(){
    return{
      axios,
      discs: [],

    }
  },
  created(){
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
    .then(res => {
      this.discs = res.data;
      console.log(res.data);
    })
    .catch(err => {
      console.log(err);
    })
  }
};
</script>

<style lang="scss">
@import '~bootstrap/scss/bootstrap.scss'
</style>
