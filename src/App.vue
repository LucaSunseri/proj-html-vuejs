<template>
    <div>
        <Header />
        <CarouselProva />
        <Main />
        <Footer />
        <Arrow />
    </div>
</template>

<script>
import Header from "./components/Header.vue";
import CarouselProva from "./components/CarouselProva.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";
import Arrow from "./components/general/Arrow.vue";

export default {
    name: "App",
    components: {
        Header,
        CarouselProva,
        Main,
        Footer,
        Arrow,
    },
};
</script>

<style lang="scss">
@import "./assets/style/general.scss";
</style>
