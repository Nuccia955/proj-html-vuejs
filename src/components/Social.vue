<template>
    <div class="external-contacts mt-3">
        <a @click.prevent class="social-btn" href="/">
            <i class="fab fa-facebook-f"></i>
        </a>
        <a @click.prevent class="social-btn" href="/">
            <i class="fab fa-instagram"></i>
        </a>
        <a @click.prevent class="social-btn" href="/">
            <i class="fab fa-twitter"></i>
        </a>
        <a @click.prevent class="social-btn" href="/">
            <i class="fab fa-youtube"></i>
        </a>
    </div>
</template>

<script>
export default {
    name: 'Social',
}
</script>

<style scoped lang="scss">
@import "../../styles/colors.scss";
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
            &:hover {
                transform: scale(1.2);
            }
        }
    }
</style>