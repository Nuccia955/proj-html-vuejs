<template>
    <footer>
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
            <div class="external-contacts mt-3">
                <a class="social-btn" href="/">
                    <i class="fab fa-facebook-f"></i>
                </a>
                <a class="social-btn" href="/">
                    <i class="fab fa-instagram"></i>
                </a>
                <a class="social-btn" href="/">
                    <i class="fab fa-twitter"></i>
                </a>
                <a class="social-btn" href="/">
                    <i class="fab fa-youtube"></i>
                </a>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
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
    .external-contacts {
        a.social-btn {
            margin-right: 10px;
            padding: 5px 12px;
            display: inline-block;
            border-radius: 50%;
            background-color: white;
            color: $goldenrod;
            font-size: 1.5em;
            &:last-child {
                margin-right: 0;
            }
            i {
                width: 25px;
                height: 25px
            }
        }
    }
}

</style>