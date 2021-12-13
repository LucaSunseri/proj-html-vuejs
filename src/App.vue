<template>
    <div>
        <Header />
        <Carousel />
        <Main />
        <Footer />
    </div>
</template>

<script>
import Header from "./components/Header.vue";
import Carousel from "./components/Carousel.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
    name: "App",
    components: {
        Header,
        Carousel,
        Main,
        Footer,
    },
};
</script>

<style lang="scss">
@import "./assets/style/general.scss";
</style>
