<template>
    <ul>
        <li>
            <a 
            @click.prevent="filterGenre"
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
 
</template>

<script>
export default {
    name: 'Search',
    props:{
        disc2: Object
    },
    methods:{
        filterGenre(){
            
        }
    }
}
</script>

<style lang="scss" scoped>

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