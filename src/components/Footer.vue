<template>
    <footer>
        <JoinUs />
        <!-- logo -->
        <div class="logo text-center py-4">
            <img class="col-2 display-block" src="../assets/avada-charity-mobile-logo-retina.png" alt="logo">
        </div>

        <div class="footer text-center py-4">
        <!-- copyrights -->
            <span class="copyrights">
                &#169; Copyright 2012 - 2020 AVADA THEME BY THEME FUSION
                | ALL RIGHTS RESERVED |
                POWERED BY WORDPRESS
            </span>

        <!-- external contacts links -->
            <Social />
        </div>
    </footer>
</template>

<script>
import JoinUs from '@/components/JoinUs.vue'
import Social from '@/components/Social.vue'
export default {
    name: 'Footer',
    components: {
        JoinUs,
        Social,
    }
}
</script>

<style scoped lang="scss">
@import "../../styles/colors.scss";
.footer {
    background-color: #f5f5f5;
    color: $french_gray;
    .copyrights {
        font-size: 0.6em;
        font-family: 'Montserrat', sans-serif;
        letter-spacing: 2px;
    }
}
</style>