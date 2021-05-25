<template>
  <div><ul>
      <li>
        <a 
        @click.prevent="filterGenre('pop')"
        href="#">pop</a>
      </li>
      <li>
        <a href="#">rock</a>
      </li>
      <li>
        <a href="#">jazz</a>
      </li>
      <li>
        <a href="#">metal</a>
      </li>
    </ul>

    <div>
      <div>Contatore: {{counter}}</div>
      <div>Pari: {{pari}}</div>
      <button @click="counter++">Incrementa di 1</button>
    </div>
  </div>
</template>

<script>
export default {
    name: 'Search',
    data: function() {
      return {
        counter: 0
      }
    },
    computed: {
      pari: function() {
        if(this.counter % 2 === 0) {
          return 'è pari'
        } else {
          return 'non è pari'
        }
      }
    },
    props:{
        disc2: Object,
    },
    methods:{
        filterGenre(genre){
            this.$emit('searchGenre', genre);
        }
    }
}
</script>

<style lang="scss" scoped>
div {
  color: white;
}
ul{
    display: flex;
    list-style: none;
}
li{
    margin: 10px;
    a{
        text-decoration: none;
        color: white;
        text-transform: uppercase;
        font-size: 1.5em;
    }
}

</style>