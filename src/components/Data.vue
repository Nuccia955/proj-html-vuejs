<template>
    <div class="data text-center mb-4">
        <div class="number">
            <i :class="`${icon}`"></i>
            {{ number }}
        </div>
        <span>{{ label }}</span>
    </div>
</template>

<script>
export default {
    name: 'Data',
    props: {
        icon: String,
        number: String,
        label: String,
    }
}
</script>

<style scoped lang="scss">
    .data {
        color: white;
        .number {
            font-size: 2em;
        }
    }
</style>