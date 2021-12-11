<template>
    <main>
        <!-- section project statistics -->
        <ProjectStatistics />

        <!-- section project values -->
        <ProjectValues />

        <!-- section recent causes gallery -->
        <CausesGallery />

        <!-- section articles -->
        <Articles />
    </main>
</template>

<script>
import ProjectStatistics from '@/components/ProjectStatistics.vue'
import ProjectValues from '@/components/ProjectValues.vue'
import CausesGallery from '@/components/CausesGallery.vue'
import Articles from '@/components/Articles.vue'

export default {
    name: 'Main',
    components: {
        ProjectStatistics,
        ProjectValues,
        CausesGallery,
        Articles,
    },
}
</script>

<style scoped lang="scss">
</style>