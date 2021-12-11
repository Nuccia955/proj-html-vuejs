<template>
    <section class="project-statistics container-fluid">
                <div class="row">
                    <div class="text col-6 offset-1 py-5">
                        <SectionTitle 
                            title="Every moment counts"
                        />
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam ipsam, perferendis tempora aperiam quos quisquam numquam iure nam mollitia ipsa illum earum temporibus. Incidunt atque aliquid, dignissimos ducimus iusto corrupti!</p>

                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis amet culpa soluta quia modi expedita et tempora temporibus reprehenderit, dolor illo nesciunt aut? Animi cum autem dolore unde iste quis.</p>

                        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Vero, culpa vitae consequuntur temporibus sunt quia quod esse quae officiis</p>

                        <BtnFilled 
                            text="Our Mission"
                        />
                    </div>

                    <div class="statistics col-4 offset-1 d-flex flex-column justify-content-center align-items-center">
                        <Data v-for="(data, index) in statistics"
                            :key="`data-${index}`"
                            :icon="data.icon"
                            :number="data.number"
                            :label="data.label"
                        />
                    </div>
                </div>
        </section>
</template>

<script>
import SectionTitle from '@/components/SectionTitle.vue'
import BtnFilled from '@/components/BtnFilled.vue'
import Data from '@/components/Data.vue'
export default {
    name: 'ProjectStatistics',
    components: {
        SectionTitle,
        BtnFilled,
        Data,
    },
    data() {
        return {
             statistics: [
                {
                    icon: 'far fa-heart',
                    number: '2032',
                    label: 'Volunteers worldwide'
                },
                {
                    icon: 'fas fa-globe',
                    number: '132',
                    label: 'Active projects'
                },
                {
                    icon: 'fas fa-dollar-sign',
                    number: '3.8M',
                    label: 'Donated'
                },
            ],
        }
    }
}
</script>

<style scoped lang="scss">
    .project-statistics {
        .statistics {
            background-image: url('../assets/home-content-bg-1.jpg');
            background-size: cover;
            background-position: center;
        }
    }
</style>