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
    <div class="ms_container">
        <div class="card my-3 " style="width: 18rem;">
            <img :src="image" alt="name" class="card-img-top">
            <div class="card-body text-center bg-black text-white">
                <h1 class="fs-5 ">{{ name }}</h1>
                <h4>{{ archetype }}</h4>
            </div>
        </div>

    </div>
</template>

<style lang="scss" scoped>
.ms_container {
    display: flex;
    flex-wrap: wrap;








}
</style>