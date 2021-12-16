<template>
  <header>
      <div class="container">
        <img src="../../assets/img/spotify-logo.png" alt="logo-spotify">
      </div>
  </header>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style lang="scss" scoped>

header {
    height: 5vh;
    background: #2e3a46;
    
    .container {
        width: 95%;
        height: 100%;
        margin: 0 auto;
        display: flex;
        align-items: center;

        img {
            width: 35px;
        }
    }
}

</style>