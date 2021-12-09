<template>
    <main>
        <!-- section project numbers -->
        <section class="project-numbers">
                <div class="row">
                    <div class="text col-6 offset-1 py-5">
                        <h2>Every Moment Counts</h2>
                        <hr class="col-2">
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam ipsam, perferendis tempora aperiam quos quisquam numquam iure nam mollitia ipsa illum earum temporibus. Incidunt atque aliquid, dignissimos ducimus iusto corrupti!</p>

                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis amet culpa soluta quia modi expedita et tempora temporibus reprehenderit, dolor illo nesciunt aut? Animi cum autem dolore unde iste quis.</p>

                        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Vero, culpa vitae consequuntur temporibus sunt quia quod esse quae officiis</p>
                    </div>

                    <div class="statistics col-4 offset-1 d-flex flex-column justify-content-center align-items-center">
                        <div class="data text-center">
                            <div class="number">
                                <i class="far fa-heart"></i>
                                2032
                            </div>
                            <span>Volunteers worldwide</span>
                        </div>
                        <div class="data text-center">
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
                                <span>Donated</span>
                            </div>
                        </div>
                    </div>
                </div>
        </section>
        <!-- section project values -->

        <!-- section recent causes gallery -->

        <!-- section articles -->

        <!-- section participation -->
    </main>
</template>

<script>
export default {
    name: 'Main',
}
</script>

<style scoped lang="scss">
@import "../../styles/colors.scss";

main {
    .project-numbers {
        hr {
            color: $goldenrod;
            opacity: 1;
            border: 2px solid;
        }
        .statistics {
            background-image: url('../assets/home-content-bg-1.jpg');
            background-size: cover;
            background-position: center;
        }
    }
}

</style>