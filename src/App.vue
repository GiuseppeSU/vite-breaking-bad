<script>
import axios from 'axios';
import MyHeader from './components/MyHeader.vue';
import MyMain from './components/MyMain.vue';
import { store } from './store.js'
import ListCard from './components/ListCard.vue';
import Card from './components/Card.vue';

export default {
  components: {
    MyHeader,
    MyMain,
    ListCard,
    Card
  },
  data() {
    return {
      store

    }
  },
  created() {
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?name=Dark Magician')
      .then(response => {
        this.store.listCard = response.data
        console.log(this.store)

      })

  }
}

</script>

<template>
  <header>
    <MyHeader></MyHeader>
  </header>

  <main>
    <MyMain></MyMain>
    <ListCard></ListCard>
    <Card></Card>

  </main>

  <footer></footer>
</template>

<style scoped lang="scss">
@use './styles/general.scss';
</style>
