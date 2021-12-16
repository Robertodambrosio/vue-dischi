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
        text-align: center;
        margin-top: 20px;
        background-color: #2e3a46; 
        padding: 15px; 
        
        img{
            width: 100%;
            margin-bottom: 20px;
            filter: grayscale(100%);
            transition: all 0.3s ease-in-out;
            cursor: pointer;

            &:hover {
                filter: grayscale(0%);
                transform: scale(1.1);
            }
        }

        h4 {
            color: white;
            margin-bottom: 30px;
            text-transform: uppercase;
        }

        p{
            font-size: 12px;
            color: #888;
        }
    }
</style>