<template>
    <div class="picture mx-2">
        <img 
            :src="require(`../assets/${img}-featured-400x300.jpg`)"
            class="d-block"
        >
        <div class="overlay d-flex justify-content-center align-items-center">
            <span>{{ text }}</span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Picture',
    props: {
        img: String,
        text: String,
    },
}
</script>

<style scoped lang="scss">
@import "../../styles/colors.scss";
.picture {
    position: relative;
    &:hover {
        .overlay {
            cursor: pointer;
            width: 100%;
            color: white;
            span {
                color: white;
                width: 100%;
            }
        }
    }
}
.overlay {
    width: 0%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
    background-color: rgba($color: $goldenrod, $alpha: .8);
    transition: width 0.2s ease-in-out;
    span {
        width: 0%;
        color: transparent;
        text-transform: uppercase;
        letter-spacing: 2px;
        font-size: 20px;
    }
}
</style>