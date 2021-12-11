<template>
    <a @click.prevent href="/" class="expand-content w-100 d-inline-block text-center text-uppercase text-decoration-none">
        {{ text }}
    </a>
</template>

<script>
export default {
    name: 'BtnExpandContent',
    props: {
        text: String,
    }
}
</script>

<style scoped lang="scss">
@import "../../styles/colors.scss";
.expand-content {
    font-weight: 300;
    letter-spacing: 3px;
    color: white;
    background-color: $burnt_sienna;
    &:hover {
        background-color: #e0635d;
    }
}
</style>