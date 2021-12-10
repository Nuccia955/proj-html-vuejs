<template>
    <main>
        <!-- section project statistics -->
        <section class="project-statistics container-fluid">
                <div class="row">
                    <div class="text col-6 offset-1 py-5">
                        <SectionTitle 
                            title="Every moment counts"
                        />
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam ipsam, perferendis tempora aperiam quos quisquam numquam iure nam mollitia ipsa illum earum temporibus. Incidunt atque aliquid, dignissimos ducimus iusto corrupti!</p>

                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis amet culpa soluta quia modi expedita et tempora temporibus reprehenderit, dolor illo nesciunt aut? Animi cum autem dolore unde iste quis.</p>

                        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Vero, culpa vitae consequuntur temporibus sunt quia quod esse quae officiis</p>

                        <a href="/" class="btn ms-btn gold">Our Mission</a>
                    </div>

                    <div class="statistics col-4 offset-1 d-flex flex-column justify-content-center align-items-center">
                        <div class="data text-center mb-4">
                            <div class="number">
                                <i class="far fa-heart"></i>
                                2032
                            </div>
                            <span>Volunteers worldwide</span>
                        </div>
                        <div class="data text-center mb-4">
                            <div class="number">
                                <i class="fas fa-globe"></i>
                                132
                            </div>
                            <span>Active projects</span>
                        </div>
                        <div class="data text-center">
                            <div class="number">
                                <i class="fas fa-dollar-sign"></i>
                                3.8M
                            </div>
                            <span>Donated</span>
                        </div>
                    </div>
                </div>
        </section>

        <!-- section project values -->
        <section class="project-values d-flex flex-column justify-content-center">
            <SectionTitle
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

        <!-- section recent causes gallery -->
        <section class="causes-gallery text-center">
            <SectionTitle
                title="Recent Causes"
                subtitle="We run projects in over 30 countries in 5 continents"
                position="center"
            />
            <div class="gallery d-flex justify-content-center">
                <div class="picture mx-2">
                    <img src="../assets/avada-charity-fair-trade-featured-400x300.jpg" alt="image">
                </div>
                <div class="picture mx-2">
                    <img src="../assets/avada-charity-shelter-featured-400x300.jpg" alt="image">
                </div>
                <div class="picture mx-2">
                    <img src="../assets/avada-charity-farming-featured-400x300.jpg" alt="image">
                </div>
                <div class="picture mx-2">
                    <img src="../assets/avada-charity-vaccines-featured-400x300.jpg" alt="image">
                </div>
            </div>
            <a href="/" class="text-uppercase">View all our causes</a>
        </section>
        <!-- section articles -->

        <!-- section participation -->
    </main>
</template>

<script>
import SectionTitle from '@/components/SectionTitle.vue'
import Card from '@/components/Card.vue'
export default {
    name: 'Main',
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
@import "../../styles/colors.scss";

main {
    .project-statistics {
        .statistics {
            background-image: url('../assets/home-content-bg-1.jpg');
            background-size: cover;
            background-position: center;
            .data {
                color: white;
                .number {
                    font-size: 2em;
                }
            }
        }
    }

    .project-values {
        height: 100vh;
        background-image: url('../assets/home-content-bg-2.jpg');
        background-size: cover;
        background-position: center;
        color: white;
        .values-list {
            max-width: 80%;
            margin: 6em auto;
        }
    }

    .causes-gallery {
        .gallery {
            padding: 5em 0 6em;
            max-width: 80%;
            margin: 0 auto;
        }
        a {
            display: inline-block;
            width: 100%;
            padding: 3em;
            background-color: $burnt-sienna;
            color: white;
            text-decoration: none;
            letter-spacing: 3px;
            font-weight: 300;
            &:hover {
                background-color: #e0635d;
            }
        }
    }
}

</style>