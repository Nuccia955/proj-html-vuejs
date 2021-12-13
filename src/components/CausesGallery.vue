<template>
    <section class="causes-gallery text-center" id="causes">
        <SectionTitle class="mt-5"
            title="Recent Causes"
            subtitle="We run projects in over 30 countries in 5 continents"
            position="center"
        />
        <div class="gallery d-flex justify-content-center">
            <Picture v-for="(picture, index) in gallery"
                :key="`picture-${index}`"
                :img="picture.url"
                :alt="picture.title"
                :text="picture.title"
            />
        </div>
        <BtnExpandContent class="py-5"
            text="View all our causes"
        />
    </section>
</template>

<script>
import SectionTitle from '@/components/SectionTitle.vue'
import Picture from '@/components/Picture.vue'
import BtnExpandContent from '@/components/BtnExpandContent.vue'
export default {
    name: 'CausesGallery',
    components: {
        SectionTitle,
        Picture,
        BtnExpandContent,
    },
    data() {
        return {
            gallery: [
                {
                    url: 'avada-charity-fair-trade',
                    title: 'fair trade'
                },
                {
                    url: 'avada-charity-shelter',
                    title: 'shelter'
                },
                {
                    url: 'avada-charity-farming',
                    title: 'farming'
                },
                {
                    url: 'avada-charity-vaccines',
                    title: 'vaccines'
                },
            ],
        }
    }
}
</script>

<style scoped lang="scss">
.causes-gallery {
    .gallery {
        padding: 5em 0 6em;
        max-width: 80%;
        margin: 0 auto;
    }
}
</style>