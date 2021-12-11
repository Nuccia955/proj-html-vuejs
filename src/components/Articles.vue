<template>
    <section class="articles">
        <SectionTitle class="section-title mt-5"
            title="Latest Articles"
            subtitle="Together we all make the difference"
            position="center"
        />
        <div class="contents d-flex py-4">
            <Article 
                :img="articles[activeIndex].urlCover"
                :title="articles[activeIndex].title"
                :text="articles[activeIndex].text"
            />
            <ul class="article-list overflow-auto">
                <ArticlePreview v-for="(article, index) in articles"
                    :key="`article-${index}`"
                    :index="index"
                    :class="{active : activeIndex === index}"
                    :cover="article.urlPreview"
                    :title="article.title"
                    :text="article.subtitle"
                    @getIndex="showArticleActive"
                />
            </ul>
        </div>
        <BtnExpandContent class="py-3"
            text="View all our articles"
        />
    </section>
</template>

<script>
import SectionTitle from '@/components/SectionTitle.vue'
import BtnExpandContent from '@/components/BtnExpandContent.vue'
import Article from '@/components/Article.vue'
import ArticlePreview from '@/components/ArticlePreview.vue'
export default {
    name: 'Aricles',
    components: {
        SectionTitle,
        BtnExpandContent,
        Article,
        ArticlePreview,
    },
    data() {
        return {
            articles: [
                {
                    urlCover: 'photo-1444213007800-cff19e1677ac-600x450',
                    urlPreview: 'photo-1444213007800-cff19e1677ac-600x450',
                    title: 'Understanding community complexities ',
                    subtitle: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro iure fugiat eaque veritatis inventore quisquam',
                    text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro iure fugiat eaque veritatis inventore quisquam et odio architecto eligendi obcaecati ab eveniet laboriosam dicta vero, ex quam aut aliquid. Reprehenderit!',
                },
                {   
                    urlCover: 'humanity-uniqueness',
                    urlPreview: 'photo-1444664597500-035db93e2323-177x142',
                    title: 'The human story of uniqueness ',
                    subtitle: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro iure fugiat eaque veritatis inventore quisquam',
                    text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro iure fugiat eaque veritatis inventore quisquam et odio architecto eligendi obcaecati ab eveniet laboriosam dicta vero, ex quam aut aliquid. Reprehenderit!',
                },
                {
                    urlCover: 'Vietnam-Market',
                    urlPreview: 'photo-1447430617419-95715602278e-177x142',
                    title: 'Sustainable trade tactics',
                    subtitle: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro iure fugiat eaque veritatis inventore quisquam',
                    text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro iure fugiat eaque veritatis inventore quisquam et odio architecto eligendi obcaecati ab eveniet laboriosam dicta vero, ex quam aut aliquid. Reprehenderit!',
                },
                {
                    urlCover: 'Women_In_Agriculture',
                    urlPreview: 'photo-1460230525622-630fe3294cd7-177x142',
                    title: 'Farmers making a difference',
                    subtitle: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro iure fugiat eaque veritatis inventore quisquam',
                    text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro iure fugiat eaque veritatis inventore quisquam et odio architecto eligendi obcaecati ab eveniet laboriosam dicta vero, ex quam aut aliquid. Reprehenderit!',
                },
                {   
                    urlCover: 'photo-1460600421604-5e138c208b9c',
                    urlPreview: 'photo-1460600421604-5e138c208b9c-177x142',
                    title: 'Meeting remotes tribes in Peru',
                    subtitle: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro iure fugiat eaque veritatis inventore quisquam',
                    text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Porro iure fugiat eaque veritatis inventore quisquam et odio architecto eligendi obcaecati ab eveniet laboriosam dicta vero, ex quam aut aliquid. Reprehenderit!',
                },
            ],
            activeIndex: 0,
        }
    },
    methods: {
        showArticleActive(index) {
            this.activeIndex = index;
        }
    }
}
</script>

<style scoped lang="scss">
@import "../../styles/colors.scss";
.articles {
    width: 70%;
    margin: 0 auto;
    .contents {
        max-height: 650px;
        .article-list {
            width: calc(50% - 20px);
            max-height: 100%;
            padding: 0;
            overflow-y: auto;
            .active {
                border: 2px solid $goldenrod;
            }
        }
    }
}
</style>