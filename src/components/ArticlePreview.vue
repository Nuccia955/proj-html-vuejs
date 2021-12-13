<template>
    <li class="article d-flex"
        @click="getIndex"
    >
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
        index: Number,
    },
    methods: {
        getIndex() {
            this.$emit('getIndex', this.index)
        }
    }
}
</script>

<style scoped lang="scss">
@import "../../styles/colors.scss";
.article {
    max-height: 96px;
    overflow-y: hidden;
    margin-bottom: 20px;
    border: 2px solid transparent;
    .cover {
        margin-right: 20px;
        &:hover {
            cursor: pointer;
            img {
                z-index: 2;
                transform: scale(1.2);
            }
        }
    }
    .text .title {
        color: $goldenrod;
    }
}
</style>