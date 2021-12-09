<template>
    <header class="d-flex flex-column align-items-center">
        <!-- nav -->
        <nav class="container-lg d-flex justify-content-between align-items-center position-fixed top-0">
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
                    <a class="btn px-4" href="/">Donate</a>
                </li>
            </ul>
        </nav>

        <!-- hero -->
        <section class="hero flex-grow-1 d-flex flex-column justify-content-center align-items-center">
            <h1 class="text-uppercase mb-4">Make a difference</h1>
            <span class="mb-4">As long as poverty, injustice & inequality persist, none of us can truly rest </span>
            <div class="actions">
                <a href="/" class="btn px-4 me-3">Our mission</a>
                <a href="/" class="btn px-4">Donate Now</a>
            </div>
        </section>
    </header>
</template>

<script>
export default {
    name: 'Header',
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
        padding: 1em 0;
        .links {
            list-style: none;
            li {
                margin: 0 2em;
                a {
                    font-size: 0.8em;
                    text-transform: uppercase;
                    display: inline-block;
                    text-decoration: none;
                    color: white;
                    &:hover {
                        color: $goldenrod;
                    }
                    &.btn {
                        outline: none;
                        font-size: 0.8em;
                        border-radius: 0;
                        background-color: $goldenrod;
                        color: white;
                        &:hover {
                            background-color: #fcd66cd7;
                        }
                    }
                }
            }
        }
    }
    .hero {
        a {
            font-size: 0.8em;
            text-transform: uppercase;
            color: white;
            border: 2px solid currentColor;
            border-radius: 0;
            &:hover {
                color: $goldenrod;
            }
        }
    }
}

</style>