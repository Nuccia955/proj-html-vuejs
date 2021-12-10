<template>
    <div id="app">
        <Header />

        <Main />

        <Footer />
    </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Main from '@/components/Main.vue'
import Footer from '@/components/Footer.vue'

export default {
    name: 'App',
    components: {
      Header,
      Main,
      Footer,
    }
}
</script>

<style lang="scss">
@import "../styles/colors.scss";

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

img {
  max-width: 100%;
}

#app {
    font-family: 'Raleway', sans-serif;
    cursor: default;
    a.btn.ms-btn {
        color: white;
        font-size: 0.8em;
        font-weight: 300;
        letter-spacing: 2px;
        padding: 0.5em 2em;
        text-transform: uppercase;
        border-radius: 0;
        outline: none;
        &.gold {
            background-color: $goldenrod;
            &:hover {
                background-color: #fcd66cd7;
            }
        }
    }
    p {
      word-spacing: 2px;
      font-size: 0.8em;
      line-height: 2.5em;
    }
}
</style>
