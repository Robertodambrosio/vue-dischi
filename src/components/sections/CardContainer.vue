<template>
  <div class="container">
    <div class="card-container">
      <Card v-for="(song, i) in card" :key="i" :card="song"/>
  </div>
  </div>
</template>

<script>
import axios from 'axios';
import Card from '../commons/Card.vue';

  export default {
    name: "CardContainer",
    components: {
        Card
    },
    data() {
        return {
            card: null
        }
    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
            // handle success
            this.card = response.data.response;
        })
        .catch(function (error) {
            // handle error
            console.log(error);
        });
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