<template>
  <div class="container">
    <SelectGenre  @change="searchGenres"/>
    <div class="card-container">
      <Card v-for="(song, i) in filtered" :key="i" :card="song"/>
  </div>
  </div>
</template>

<script>
import axios from 'axios';
import Card from '../commons/Card.vue';
import SelectGenre from '../commons/SelectGenre.vue';

  export default {
    name: "CardContainer",
    components: {
        Card,
        SelectGenre
    },
    data() {
        return {
            card: null,
            selectVal: ''
        }
    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
            this.card = response.data.response;
        })
        .catch(function (error) {
            console.log(error);
        });
    },
    methods: {
        searchGenres(payload) {
            this.selectVal = payload;
        }
    },
         computed: {
         filtered() {
           console.log(this)
             return this.card.filter((elm) => {
                 return elm.genre.toLowerCase().includes(this.selectVal.toLowerCase()); 
             } );  
         }
     }
  };
</script>

<style lang="scss" scoped>
  .container {
    width: 60%;
    margin: auto;

    .card-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-around;
    }
  }
</style>