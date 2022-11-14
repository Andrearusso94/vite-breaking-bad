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
        <div class="character my-2">
            <img class="my-2" :src="character.img" :alt="character.name">
            <h5 class="text-white">{{ character.name }}</h5>

            <div class="description p-2">
                <h4 class="text-secondary">{{ character.category }}</h4>
                <p class="text-secondary">{{ character.status }}</p>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.character {
    img {
        width: 175px;
        height: 225px;
    }

    background-color: #2e3a46;
    width: 80%;
    text-align: center;

    p {
        margin-top: -12px;
    }
}
</style>