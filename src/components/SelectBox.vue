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
    <select v-model="store.category" @change="$emit('searchData')" class="form-select form-select-sm" name="" id="">

        <option value="Breaking Bad">Breaking Bad</option>
        <option value="Better Call Saul">Better Call Saul</option>

    </select>
</template>