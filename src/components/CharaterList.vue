<script>
import CharaterItemVue from './CharaterItem.vue';
import { store } from '../store.js'
export default {
    name: 'CharaterList',
    components: {
        CharaterItemVue
    },
    data() {
        return {
            store
        }
    }

}
</script>

<template>
    <div class="container py-5 bg-white">
        <div class="row row-cols-1 row-cols-sm-5">
            <CharaterItemVue :character="character" v-for="character in store.characters"></CharaterItemVue>
        </div>
    </div>
</template>

<style lang="scss" scoped>

</style>