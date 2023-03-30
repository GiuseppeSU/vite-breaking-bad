<script>
import axios from 'axios';
import MyHeader from './components/MyHeader.vue';
import MyMain from './components/MyMain.vue';
import { store } from './store.js'
import ListCard from './components/ListCard.vue';


export default {
  components: {
    MyHeader,
    MyMain,
    ListCard,

  },
  data() {
    return {
      store,
      baseUrl: "https://db.ygoprodeck.com/api/v7/"


    }
  },
  methods: {
    getCards(archeType) {
      console.log(archeType)

      let urlApi = this.baseUrl + "cardinfo.php?sort=name&num=25&offset=0"
      if (archeType) {
        urlApi += '&archetype=' + archeType
      }
      axios.get(urlApi)
        .then(response => {
          this.store.listCard = response.data
          console.log(this.store)
        });
    },
    getArchetype() {
      let urlType = this.baseUrl + "archetypes.php"
      axios.get(urlType)
        .then(response => {
          this.store.archetype = response.data
          console.log(this.store.archetype)
        });

    }
  },
  created() {
    this.getCards();
    this.getArchetype();


  }

}


</script>

<template>
  <header>
    <MyHeader></MyHeader>
  </header>

  <main>
    <MyMain @select="getCards"></MyMain>
    <ListCard></ListCard>


  </main>

  <footer></footer>
</template>

<style scoped lang="scss">
@use './styles/general.scss';
</style>
