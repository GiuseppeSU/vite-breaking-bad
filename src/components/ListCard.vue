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
    <div class=" ms-color">
        <div v-for="(card, index) in store.listCard.data" :key="index">

            <Card class="ms-5" v-for=" (image, index) in card.card_images" :image="image.image_url" :name="card.name"
                :archetype="card.archetype" :key="index">
            </Card>
        </div>

    </div>
</template>

<style lang="scss" scoped>
.ms-color {
    background-color: rgb(212, 143, 56);
    display: flex;
    flex-wrap: wrap;
    justify-content: center;

}
</style>