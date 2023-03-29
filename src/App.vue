<script>
import MyHeader from './components/MyHeader.vue';
import MyMain from './components/MyMain.vue';
export default {
  components: {
    MyHeader,
    MyMain
  }
}

</script>

<template>
  <header>
    <MyHeader></MyHeader>
  </header>

  <main>
    <MyMain></MyMain>

  </main>

  <footer></footer>
</template>

<style scoped lang="scss">
@use './styles/general.scss';
</style>
