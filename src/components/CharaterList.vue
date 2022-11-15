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
        <div class="alert bg-dark text-white" v-if="store.characters !== null">Found {{ store.characters.length }}
            characters</div>
        <div class="row row-cols-1 row-cols-sm-5 mx-2">
            <CharaterItemVue :character="character" v-for="character in store.characters"></CharaterItemVue>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.container {
    width: 80%;
}
</style>