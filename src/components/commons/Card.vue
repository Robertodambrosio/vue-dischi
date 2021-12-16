<template>
  <div class="card-song">
      <img :src="card.poster" :alt="card.title">
      <h4>{{card.title}}</h4>
      <p>{{card.author}}</p>
      <p>{{card.year}}</p>
  </div>
</template>

<script>
export default {
name: 'Card',
props: {
    card: Object
}
}
</script>

<style lang="scss" scoped>
    .card-song {
        max-width: calc(20% - 20px);
        min-height: 350px;
        margin-bottom: 20px;
        text-align: center;
        background-color: #2e3a46; 
        padding: 15px; 
        
        img{
            width: 100%;
            margin-bottom: 10px;
        }

        h4 {
            color: white;
            margin-bottom: 10px;
            text-transform: uppercase;
        }

        p{
            font-size: 12px;
            color: #888;
        }
    }
</style>