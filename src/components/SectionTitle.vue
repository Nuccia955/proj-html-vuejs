<template>
    <div class="title" :class="{ 'text-center': position === 'center' }">
        <h2 class="text-uppercase">
            {{ title }}
        </h2>
        <hr class="col-2" :class="{ 'mx-auto': position === 'center'}">
        <span>
            {{ subtitle }}
        </span>
    </div>
</template>

<script>
export default {
    name: 'SectionTitle',
    props: {
        title: String,
        subtitle: String,
        position: String,
    }
}
</script>

<style scoped lang="scss">
@import "../../styles/colors.scss";
    hr {
        color: $goldenrod;
        opacity: 1;
        border: 2px solid;
        margin: 1em 0 2em;
    }
</style>