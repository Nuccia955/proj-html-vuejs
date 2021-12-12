<template>
    <header class="d-flex flex-column align-items-center" id="header"
        :class="{ height100: status }">
        <!-- nav -->
        <nav class="position-fixed top-0 w-100">
            <div class="container-lg d-flex justify-content-between align-items-center">
                <div class="logo col-2">
                    <a href="#header">
                        <img src="../assets/avada-charity-logo-retina.png" alt="logo">
                    </a>
                </div>
                <ul class="links d-md-flex align-items-center m-0">
                    <li>
                        <a href="#header">Home</a>
                    </li>
                    <li>
                        <a href="#mission">Mission</a>
                    </li>
                    <li>
                        <a href="#causes">Causes</a>
                    </li>
                    <li>
                        <a href="#journal">Journal</a>
                    </li>
                    <li>
                        <BtnFilled
                            text="Donate" 
                        />
                    </li>
                </ul>
            </div>
        </nav>

        <!-- hero -->
        <section v-if="status" class="hero flex-grow-1 d-flex flex-column justify-content-center align-items-center">
            <h1 class=" text-uppercase">Make a difference</h1>
            <span>As long as poverty, injustice & inequality persist, none of us can truly rest.</span>
            <div class="actions mt-4">
                <BtnBordered class="me-3"
                    text="Our mission"
                />
                <BtnBordered 
                    text="Donate Now"
                />
            </div>
        </section>
    </header>
</template>

<script>
import BtnBordered from '@/components/BtnBordered.vue'
import BtnFilled from '@/components/BtnFilled.vue'
export default {
    name: 'Header',
    components: {
        BtnBordered,
        BtnFilled,
    },
    props: {
        status: Boolean,
    }
}
</script>

<style scoped lang="scss">
@import "../../styles/colors.scss";

header {
    h1 {
        letter-spacing: 3px;
        font-weight: 300;
    }
    color: white;
    background-image: url('../assets/home-page-slider.jpg');
    background-position-x: center;
    background-size: cover;
    &.height100 {
        height: 100vh;
    }
    nav {
        background-color: rgba(0, 0, 0, 0.4);
        padding: 1em 0;
        .links {
            list-style: none;
            li {
                margin: 0 2em;
                a {
                    font-size: 0.8em;
                    text-transform: uppercase;
                    letter-spacing: 2px;
                    display: inline-block;
                    text-decoration: none;
                    color: white;
                    &:hover {
                        color: $goldenrod;
                    }
                }
            }
        }
    }
}
</style>