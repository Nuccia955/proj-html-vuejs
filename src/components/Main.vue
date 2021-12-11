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
                        <Data v-for="(data, index) in statistics"
                            :key="`data-${index}`"
                            :icon="data.icon"
                            :number="data.number"
                            :label="data.label"
                        />
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
            <SectionTitle class="mt-5"
                title="Recent Causes"
                subtitle="We run projects in over 30 countries in 5 continents"
                position="center"
            />
            <div class="gallery d-flex justify-content-center">
                <Picture v-for="(picture, index) in gallery"
                    :key="`picture-${index}`"
                    :img="picture.url"
                    :alt="picture.alt"
                />
            </div>
            <a href="/" class="text-uppercase">View all our causes</a>
        </section>

        <!-- section articles -->
        <section class="articles">
            <SectionTitle class="section-title mt-5"
                title="Latest Articles"
                subtitle="Together we all make the difference"
                position="center"
            />
            <div class="contents d-flex py-4">
                <div class="active">
                    <div class="cover">
                        <img src="../assets/photo-1444213007800-cff19e1677ac-600x450.jpg" alt="image">
                    </div>
                    <div class="text">
                        <h6 class="title">Title</h6>
                        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ipsa sapiente adipisci illo nostrum, nam possimus necessitatibus? Nostrum animi laboriosam doloribus, quaerat aliquam repudiandae quidem ut deleniti! Natus nostrum accusantium maxime.</p>
                    </div>
                </div>
                <ul class="article-list overflow-auto">
                    <ArticlePreview v-for="(article, index) in articles"
                        :key="`article-${index}`"
                        :cover="article.url"
                        :title="article.title"
                        :text="article.subtitle"
                    />
                </ul>
            </div>
        </section>

        <!-- section participation -->
        <section class="join-us py-5 mt-5">
            <SectionTitle class="w-50 mx-auto mt-5"
                title="Change a life today"
                subtitle="As long as poverty, injustice & inequality persist, none of us can truly rest. It doesn't take much to change a life. get in touch today and start making the difference."
                position="center"
            />
            <div class="actions text-center mt-5">
                <a href="/" class="btn ms-btn me-3">Volunteer</a>
                <a href="/" class="btn ms-btn">Donate Now</a>
            </div>
        </section>
    </main>
</template>

<script>
import SectionTitle from '@/components/SectionTitle.vue'
import Card from '@/components/Card.vue'
import Data from '@/components/Data.vue'
import Picture from '@/components/Picture.vue'
import ArticlePreview from '@/components/ArticlePreview.vue'

export default {
    name: 'Main',
    components: {
        SectionTitle,
        Card,
        Data,
        Picture,
        ArticlePreview,
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
            gallery: [
                {
                    url: 'avada-charity-fair-trade',
                    alt: 'fair-trade'
                },
                {
                    url: 'avada-charity-shelter',
                    alt: 'shelter'
                },
                {
                    url: 'avada-charity-farming',
                    alt: 'farming'
                },
                {
                    url: 'avada-charity-vaccines',
                    alt: 'vaccines'
                },
            ],
            articles: [
                {
                    url: 'photo-1444664597500-035db93e2323',
                    title: 'The human story of uniqueness ',
                    subtitle: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro iure fugiat eaque veritatis inventore quisquam',
                    text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro iure fugiat eaque veritatis inventore quisquam et odio architecto eligendi obcaecati ab eveniet laboriosam dicta vero, ex quam aut aliquid. Reprehenderit!',
                },
                {
                    url: 'photo-1447430617419-95715602278e',
                    title: 'Sustainable trade tactics',
                    subtitle: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro iure fugiat eaque veritatis inventore quisquam',
                    text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro iure fugiat eaque veritatis inventore quisquam et odio architecto eligendi obcaecati ab eveniet laboriosam dicta vero, ex quam aut aliquid. Reprehenderit!',
                },
                {
                    url: 'photo-1460230525622-630fe3294cd7',
                    title: 'Farmers making a difference',
                    subtitle: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro iure fugiat eaque veritatis inventore quisquam',
                    text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro iure fugiat eaque veritatis inventore quisquam et odio architecto eligendi obcaecati ab eveniet laboriosam dicta vero, ex quam aut aliquid. Reprehenderit!',
                },
                {
                    url: 'photo-1460600421604-5e138c208b9c',
                    title: 'Meeting remotes tribes in Peru',
                    subtitle: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro iure fugiat eaque veritatis inventore quisquam',
                    text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro iure fugiat eaque veritatis inventore quisquam et odio architecto eligendi obcaecati ab eveniet laboriosam dicta vero, ex quam aut aliquid. Reprehenderit!',
                },
            ]
        }
    },
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

    .articles {
        width: 70%;
        margin: 0 auto;
        .contents {
            max-height: 650px;
            .active {
                border: 1px solid lightgray;
                .text {
                    padding: 15px 15px;
                    .title {
                        color: $goldenrod;
                    }
                }
            }
            .active {
                margin-right: 20px;
            }
            .article-list,
            .active {
                width: calc(50% - 20px);
                max-height: 100%;
                padding: 0;
                overflow-y: auto;
            }
        }
    }

    .join-us {
        min-height: 450px;
        color: white;
        background-image: url('../assets/home-footer.jpg');
        background-position: center;
        background-size: cover;
        a.ms-btn {
            border: 2px solid currentColor;
        }
    }
}

</style>