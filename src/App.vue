<template>
  <div id="app">
    <div class="container">
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
      this.discs = res.data.response;
      console.log(res.data);
    })
    .catch(err => {
      console.log(err);
    })
  }
};
</script>

<style lang="scss">
@import '~bootstrap/scss/bootstrap.scss';

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app{
  background-color: rgb(30, 45, 59);
  height: 100%;
  
}

</style>
