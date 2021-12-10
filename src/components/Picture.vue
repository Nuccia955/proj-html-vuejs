<template>
    <div class="picture mx-2">
        <img 
            :src="require(`../assets/${img}-featured-400x300.jpg`)"
            class="d-block"
        >
    </div>
</template>

<script>
export default {
    name: 'Picture',
    props: {
        img: String,
    },
}
</script>

<style scoped lang="scss">
</style>