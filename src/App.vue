<template>
    <div>
        <Header />
        <Carousel />
        <Main />
        <Footer />
        <ButtonFixed
            :image="'shop1.svg'"
            :alt="'Wheel'"
            :widthimg="'90%'"
            :background="'#ee2852'"
            :bottom="'570px'"
            :right="'0px'"
            :width="'2.4rem'"
            :height="'2.4rem'"
        />
        <ButtonFixed
            :image="'shop2.svg'"
            :alt="'Shopping Cart'"
            :widthimg="'60%'"
            :background="'#fff'"
            :bottom="'518px'"
            :right="'0px'"
            :width="'2.4rem'"
            :height="'2.4rem'"
        />
        <ButtonFixed
            :image="'arrow.svg'"
            :alt="'Arrow-Up'"
            :widthimg="'60%'"
            :background="'#c0e1cf'"
            :bottom="'20px'"
            :right="'10px'"
            :width="'2.8rem'"
            :height="'2.8rem'"
        />
    </div>
</template>

<script>
import Header from "./components/Header.vue";
import Carousel from "./components/Carousel.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";
import ButtonFixed from "./components/general/ButtonFixed.vue";

export default {
    name: "App",
    components: {
        Header,
        Carousel,
        Main,
        Footer,
        ButtonFixed,
    },
};
</script>

<style lang="scss">
@import "./assets/style/general.scss";
</style>
