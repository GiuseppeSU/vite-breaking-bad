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
    <div class="container">
        <div class="row">
            <div class="col-3">
                <img :src="image" alt="">
                <h1>{{ name }}</h1>
                <h4>{{ archetype }}</h4>


            </div>


        </div>
    </div>
</template>

<style lang="scss" scoped></style>