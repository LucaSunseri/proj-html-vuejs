<template>
    <div class="ls-carousel">
        <div class="container">
            <div class="row" v-for="slide in slides" :key="slide.id">
                <div class="col-12 col-lg-6 ciao" v-if="counter == slide.id">
                    <h2>
                        {{ slide.text.title }}
                        <span class="ls-title__italic">{{
                            slide.text.italic
                        }}</span>
                    </h2>
                    <p>{{ slide.text.p }}</p>
                    <div class="ls-button">
                        <span class="ls-button-text">Read more</span>
                    </div>
                </div>
                <div
                    class="col-12 col-lg-6 ls-carousel__image"
                    v-if="counter == slide.id"
                >
                    <img
                        v-for="(image, key) in slide.imageCenter"
                        :key="key"
                        :src="require(`../assets/img/${image.image}`)"
                        alt=""
                        :style="`width: ${image.width}`"
                    />
                    <div class="ls-carousel__image-absolute">
                        <img
                            v-for="(image, index) in slide.imageAbsolute"
                            :key="index"
                            :src="require(`../assets/img/${image.image}`)"
                            alt=""
                            :style="`top: ${image.top}; left: ${image.left}`"
                        />
                    </div>
                </div>
            </div>
            <div class="ls-carousel__button-side d-none d-lg-block">
                <i @click="slidePrev" class="fas fa-chevron-circle-left"></i>
                <i @click="slideNext" class="fas fa-chevron-circle-right"></i>
            </div>
        </div>

        <div class="ls-carousel__button-center">
            <i class="fas fa-circle" @click="counter = 1"></i>
            <i class="fas fa-circle" @click="counter = 2"></i>
            <i class="fas fa-circle" @click="counter = 3"></i>
        </div>
    </div>
</template>

<script>
import slides from "../assets/data/Carousel";

export default {
    name: "Carousel",
    data() {
        return {
            slides,
            counter: 1,
        };
    },
    methods: {
        slideNext() {
            console.log("ciao");
        },
        slidePrev() {
            console.log("ciao");
        },
    },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/vars.scss";

.ls-carousel {
    position: relative;
    height: 600px;
    overflow: hidden;
    .container {
        width: 80%;
        height: 90%;
        position: relative;

        h2 {
            font-size: 80px;
            font-weight: 400;
        }
        p {
            color: $color-secondary;
        }
        .ciao {
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
    }
}

.ls-carousel__button-side {
    .fas {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        font-size: 30px;
        color: #e1c0b0;
        cursor: pointer;
    }
    .fa-chevron-circle-left {
        left: -100px;
    }
    .fa-chevron-circle-right {
        right: -100px;
    }
}

.ls-carousel__image {
    position: relative;
    .ls-carousel__image-absolute {
        img {
            position: absolute;
            width: 7%;
        }
    }
}

.ls-carousel__button-center {
    display: flex;
    justify-content: center;
    .fas {
        color: #e1c0b0;
        font-size: 10px;
        padding: 10px;
        cursor: pointer;
    }
}
</style>
