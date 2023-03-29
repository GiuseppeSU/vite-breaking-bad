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
    <div class=" text-center ">
        <div class="row m-3 justify-content-center ">
            <div class="col-6 ms-color p-4">

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
    border: 1px solid black;


    .my-image {
        height: 100px;
    }

}
</style>