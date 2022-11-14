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
    <div class="container">
        <div class="row row-cols-1 row-cols-sm-4">
            <CharaterItemVue :character="character" v-for="character in store.characters"></CharaterItemVue>
        </div>
    </div>
</template>