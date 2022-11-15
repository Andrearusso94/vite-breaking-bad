<script>
import { store } from '../store.js'
export default {
    name: 'SelectBox',
    emits: ['searchData'],
    data() {
        return {
            store
        }
    }


}
</script>

<template>
    <select v-model="store.selectSeries" @change="$emit('searchData')" class="form-select form-select-sm" name="" id="">
        <option selected>breaking bad</option>
        <option value="">Better Call Soul</option>

    </select>
</template>