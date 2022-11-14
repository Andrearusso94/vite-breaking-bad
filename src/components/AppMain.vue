<script>
import CharaterListVue from './CharaterList.vue';

export default {
    name: 'AppMain',
    components: { CharaterListVue },

}
</script>
<template>
    <main>
        <section class="charaters">

            <CharaterListVue />
        </section>
    </main>
</template>