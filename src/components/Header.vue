<template>
    <header class="d-flex flex-column align-items-center">
        <!-- nav -->
        <nav class="position-fixed top-0 w-100">
            <div class="container-lg d-flex justify-content-between align-items-center">
                <div class="logo col-2">
                    <img src="../assets/avada-charity-logo.png" alt="logo">
                </div>
                <ul class="links d-md-flex align-items-center m-0">
                    <li>
                        <a href="/">Home</a>
                    </li>
                    <li>
                        <a href="/">Mission</a>
                    </li>
                    <li>
                        <a href="/">Causes</a>
                    </li>
                    <li>
                        <a href="/">Journal</a>
                    </li>
                    <li>
                        <a class="btn ms-btn gold" href="/">Donate</a>
                    </li>
                </ul>
            </div>
        </nav>

        <!-- hero -->
        <section class="hero flex-grow-1 d-flex flex-column justify-content-center align-items-center">
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
export default {
    name: 'Header',
    components: {
        BtnBordered,
    }
}
</script>

<style scoped lang="scss">
@import "../../styles/colors.scss";

header {
    color: white;
    background-image: url('../assets/home-page-slider.jpg');
    background-position-x: center;
    background-size: cover;
    height: 100vh;
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