<template>
    <a class="btn ms-btn gold" href="/">{{ text }}</a>
</template>

<script>
export default {
    name: 'BtnFilled',
    props: {
        text: String,
    }
}
</script>

<style scoped lang="scss">
@import "../../styles/colors.scss"; 
    a.gold {
        background-color: $goldenrod;
        &:hover {
            background-color: #fcd66cd7;
        }
    }
</style>