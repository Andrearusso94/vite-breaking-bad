<script>
import CharaterListVue from './CharaterList.vue';
import SelectBoxVue from './SelectBox.vue';
import { store } from '../store.js';
import axios from 'axios'
export default {
    name: 'AppMain',
    components: { CharaterListVue, SelectBoxVue },
    data() {
        return {
            store
        }
    },
    methods: {
        selectSeries() {
            console.log(this.store.selectSeries)
            const url = `${this.store.API_URL}?category=${selectSeries}`
            console.log(this.selectSeries);

            axios.get(url)
                .then(resp => {
                    this.store.characters = resp.data
                })
                .catch(err => {
                    console.error(err)

                })
        }
    }

}
</script>
<template>
    <main>
        <div class="category my-5 container">
            <div class="mb-3">

                <SelectBoxVue @searchData="selectSeries"></SelectBoxVue>
            </div>
        </div>


        <section class="charaters my-3">

            <CharaterListVue />
        </section>
    </main>
</template>

<style lang="scss">
.container {
    width: 80%;
}
</style>