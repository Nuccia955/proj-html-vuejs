<template>
    <a @click.prevent href="/" class="btn ms-btn bordered">
        {{ text }}
    </a>
</template>

<script>
export default {
    name: 'BtnBordered',
    props: {
        text: String,
    }
}
</script>

<style scoped lang="scss">
@import "../../styles/colors.scss";
    a.bordered {
        border: 2px solid currentColor;
        &:hover {
            color: $goldenrod !important;
        }
    }
</style>