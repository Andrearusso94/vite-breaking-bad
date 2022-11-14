<script>
export default {
    name: 'CharaterItem',
    props: {
        character: Object
    }
}
</script>


<template>
    <div class="col">
        <div class="character">
            <img :src="character.img" :alt="character.name">
            <h3>{{ character.name }}</h3>

            <div class="description">
                <h3>{{ character.category }}</h3>
                <h5>{{ character.status }}</h5>
            </div>
        </div>
    </div>
</template>