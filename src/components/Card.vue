<template>
    <div class="text-center px-2">
        <i :class="`${icon}`" class="mb-2"></i>
        <h5 class="mb-4">{{ title }}</h5>
        <p>{{ text }}</p>
        <a href="/" class="btn ms-btn gold">Learn More</a>
    </div>
</template>

<script>
export default {
    name: 'Card',
    props: {
        icon: String,
        title: String,
        text: String,
    }
}
</script>

<style scoped lang="scss">
@import "../../styles/colors.scss";
    i {
        color: $goldenrod;
        font-size: 2.5em;
    }
</style>