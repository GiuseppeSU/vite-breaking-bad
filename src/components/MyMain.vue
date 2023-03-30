<script>
import { store } from '../store.js'

export default {
    name: 'MyMain',

    data() {
        return {
            store

        }
    }

}
</script>

<template>
    <div class="container-fluid  mt-3 w-75 mb-3">
        <div class="row">
            <div class="col-3">
                <div class="btn-group mt-3   ">
                    <button class="btn btn-secondary dropdown-toggle " type="button" data-bs-toggle="dropdown"
                        aria-expanded="false">
                        All
                    </button>
                    <ul class="dropdown-menu  ">
                        <li v-for="atype in store.archetype"><a @click="$emit('select', atype.archetype_name)"
                                class="dropdown-item" href="#">{{ atype.archetype_name }}</a></li>

                    </ul>
                </div>


            </div>
        </div>
    </div>
</template>



<style lang="scss" scoped></style>
