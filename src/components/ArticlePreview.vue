<template>
    <li class="article d-flex">
        <div class="cover w-25">
            <img :src="require(`../assets/${cover}.jpg`)" alt="article cover">
        </div>
        <div class="text w-75 overflow-hidden">
            <h5 class="title">{{ title }}</h5>
            <p>{{ text }}</p>
        </div>
    </li>
</template>

<script>
export default {
    name: 'ArticlePreview',
    props: {
        cover: String,
        title: String,
        text: String,
    }
}
</script>

<style scoped lang="scss">
@import "../../styles/colors.scss";
.article {
    max-height: 96px;
    overflow-y: hidden;
    margin-bottom: 20px;
    .cover {
        margin-right: 20px;
    }
    .text .title {
        color: $goldenrod;
    }
}
</style>