<template>
    <div class="text-center px-2">
        <i :class="`${icon}`" class="mb-2"></i>
        <h5 class="mb-4">{{ title }}</h5>
        <p>{{ text }}</p>
        <BtnFilled 
            text="Learn More"
        />
    </div>
</template>

<script>
import BtnFilled from '@/components/BtnFilled.vue'
export default {
    name: 'Card',
    components: { 
      BtnFilled, 
    },
    props: {
        icon: String,
        title: String,
        text: String,
    },
}
</script>

<style scoped lang="scss">
@import "../../styles/colors.scss";
    i {
        color: $goldenrod;
        font-size: 2.5em;
    }
</style>