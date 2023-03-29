<script>
import Card from './Card.vue';
import { store } from '../store.js'
export default {
    name: 'ListCard',
    data() {
        return {
            store: store

        }
    },
    components: {
        Card
    }
}
</script>

<template>
    <div class="container  ms-color">
        <div class="row" v-for="(card, index) in store.listCard.data" :key="index">

            <Card class="col-sm-6" v-for=" (image, index) in card.card_images" :image="image.image_url" :name="card.name"
                :archetype="card.archetype" :key="index">
            </Card>



        </div>

    </div>
</template>

<style lang="scss" scoped>
.ms-color {
    background-color: rgb(212, 143, 56);

}
</style>