<script>
export default {
    name: 'Card',
    props: {
        image: String,
        name: String,
        archetype: String

    }
}

</script>

<template>
    <div class="container d-flex text-center ">
        <div class="row m-3">
            <div class="col ms-color  ">
                <img :src="image" alt="name" class="my-image">
                <h1>{{ name }}</h1>
                <h4>{{ archetype }}</h4>


            </div>


        </div>
    </div>
</template>

<style lang="scss" scoped>
.ms-color {
    background-color: white;

    .my-image {
        height: 100px;
    }

}
</style>