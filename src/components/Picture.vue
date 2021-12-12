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
.picture:hover {
    transform: scale(1.5);
    box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.4);
}
</style>