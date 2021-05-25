<template>
  <div class="col-sm-4 col-md-4 col-lg-2 text-center ">
      <div class="img text-center">
          <img :src="disc.poster" :alt="disc.title">
      </div>
      
      <h6>{{ disc.title }}</h6>
      <p>{{ disc.author }}</p>
      <p>{{ disc.year }}</p>

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

<style lang="scss" scoped>

    div{
        background-color: rgb(46, 58, 70);
        margin: 10px;
        padding: 10px 20px;
        .img{
        height: 100px;
        margin: 0 auto;
            img{
                height: 100%;
            }
        }
        h6{
            text-transform: uppercase;
            color: white;
            margin-top: 5px;
        }
        p{
            color: rgb(119, 120, 121);
            min-height: 20px;
        }
    }
    
</style>