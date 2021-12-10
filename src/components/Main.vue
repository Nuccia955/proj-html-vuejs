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
            <!-- <div class="title text-center">
                <h2 class="text-uppercase">Our values</h2>
                <hr class="col-2 mx-auto">
                <span>Think Big. Act Bigger</span>
            </div> -->
            <SectionTitle
                title="Our Values"
                subtitle="Think Big. Act Bigger"
                position="center"
            />
            <div class="values-list d-flex justify-content-center">
                <div class="value text-center px-2">
                    <i class="fas fa-tint mb-2"></i>
                    <h5 class="mb-4">Clean Water</h5>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Est impedit iure nemo illum iusto quasi accusamus quis aspernatur distinctio </p>
                    <a href="/" class="btn ms-btn gold">Learn More</a>
                </div>
                <div class="value text-center px-2">
                    <i class="fas fa-stethoscope mb-2"></i>
                    <h5 class="mb-4">Vaccinations</h5>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Est impedit iure nemo illum iusto quasi accusamus quis aspernatur distinctio </p>
                    <a href="/" class="btn ms-btn gold">Learn More</a>
                </div>
                <div class="value text-center px-2">
                    <i class="fas fa-graduation-cap mb-2"></i>
                    <h5 class="mb-4">Education</h5>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Est impedit iure nemo illum iusto quasi accusamus quis aspernatur distinctio </p>
                    <a href="/" class="btn ms-btn gold">Learn More</a>
                </div>
                <div class="value text-center px-2">
                    <i class="fab fa-pagelines mb-2"></i>
                    <h5 class="mb-4">Farming</h5>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Est impedit iure nemo illum iusto quasi accusamus quis aspernatur distinctio </p>
                    <a href="/" class="btn ms-btn gold">Learn More</a>
                </div>
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
export default {
    name: 'Main',
    components: {
        SectionTitle
    }
}
</script>

<style scoped lang="scss">
@import "../../styles/colors.scss";

main {
    .project-statistics {
        hr {
            color: $goldenrod;
            opacity: 1;
            border: 2px solid;
        }
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
        hr {
            opacity: 1;
            border: 2px solid $goldenrod;
        }
        .values-list {
            max-width: 80%;
            margin: 6em auto;
            .value {
                i {
                    color: $goldenrod;
                    font-size: 2.5em;
                }
                p {
                    font-size: 0.8em;
                    font-weight: 300;
                    line-height: 2.5em;
                }
            }
        }
    }

    .causes-gallery {
        .title {
            margin-top: 6em;
            hr {
                opacity: 1;
                border: 2px solid $goldenrod;
            }
        }
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