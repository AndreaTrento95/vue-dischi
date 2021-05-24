<template>
  <div class="col-sm-4 col-md-4 col-lg-3">

      <img :src="disc.poster" :alt="disc.title">
      <h2>{{ disc.title }}</h2>
      <h4>{{ disc.author }}</h4>
      <h5>{{ disc.year }}</h5>

  </div>
</template>

<script>
export default {
    name: 'Disc',
    props:{
        disc: Object
    }
}
</script>

<style>

</style>