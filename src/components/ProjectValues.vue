<template>
    <section class="project-values d-flex flex-column justify-content-center">
            <SectionTitle class="mt-5"
                title="Our Values"
                subtitle="Think Big. Act Bigger"
                position="center"
            />
            <div class="values-list d-flex justify-content-center">
                <Card v-for="(value, index) in values" 
                    :key="`value-${index}`"
                    :icon="value.icon"
                    :title="value.title"
                    :text="value.text"
                />
            </div>
        </section>
</template>

<script>
import SectionTitle from '@/components/SectionTitle.vue'
import Card from '@/components/Card.vue'
export default {
    name: 'ProjectValues',
    components: {
        SectionTitle,
        Card,
    },
    data() {
        return {
            values: [
                {
                    icon: 'fas fa-tint',
                    title: 'Clean Water',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Est impedit iure nemo illum iusto quasi accusamus quis aspernatur distinctio',
                },
                {
                    icon: 'fas fa-stethoscope',
                    title: 'Vaccinations',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Est impedit iure nemo illum iusto quasi accusamus quis aspernatur distinctio',
                },
                {
                    icon: 'fas fa-graduation-cap',
                    title: 'Education',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Est impedit iure nemo illum iusto quasi accusamus quis aspernatur distinctio',
                },
                {
                    icon: 'fab fa-pagelines',
                    title: 'Farming',
                    text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Est impedit iure nemo illum iusto quasi accusamus quis aspernatur distinctio',
                },
            ],
        }
    }
}
</script>

<style scoped lang="scss">
.project-values {
    min-height: 450px;
    background-image: url('../assets/home-content-bg-2.jpg');
    background-size: cover;
    background-position: center;
    color: white;
    .values-list {
        max-width: 80%;
        margin: 4em auto;
    }
}
</style>