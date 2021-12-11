<template>
    <div class="article-active">
        <div class="cover">
            <img :src="require(`../assets/${img}.jpg`)" alt="article cover">
        </div>
        <div class="text">
            <h6 class="title">{{ title }}</h6>
            <p>{{ text }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Article',
    props: {
        img: String,
        title: String,
        text: String,
    }
}
</script>

<style scoped lang="scss">
@import "../../styles/colors.scss";
    .article-active {
        width: calc(50% - 20px);
        max-height: 100%;
        padding: 0;
        overflow-y: auto;
        margin-right: 20px;
        border: 1px solid lightgray;
        .cover {
            img {
                width: 100%;
            }
        }
        .text {
            padding: 15px 15px;
            .title {
                color: $goldenrod;
            }
        }
    }
</style>