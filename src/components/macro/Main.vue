<template>
  <main>
      <CardContainer/>
  </main>
</template>

<script>
import CardContainer from '../sections/CardContainer.vue';

export default {
    name: 'Main',
    components: {
        CardContainer
    }
}
</script>

<style lang="scss" scoped>
main {
    height: 95vh;
    display: flex;
    align-items: center;
}
</style>