<template>
    <div class="ls-carousel">
        <div class="container">
            <div class="row">
                <!-- Section Text -->
                <div class="col-12 col-lg-6 ls-carousel__text">
                    <h2>
                        {{ slide[counter].text.title }}
                        <span class="ls-title__italic">{{
                            slide[counter].text.italic
                        }}</span>
                    </h2>
                    <p>{{ slide[counter].text.p }}</p>
                    <div class="ls-button">
                        <span class="ls-button-text">Read more</span>
                    </div>
                </div>
                <!-- Section Image -->
                <div class="col-12 col-lg-6 ls-carousel__image">
                    <img
                        v-for="(image, key) in slide[counter].imageCenter"
                        :key="key"
                        :src="require(`../assets/img/${image.image}`)"
                        alt=""
                        :style="`width: ${image.width}`"
                    />
                    <div class="ls-carousel__image-absolute">
                        <img
                            v-for="(image, index) in slide[counter]
                                .imageAbsolute"
                            :key="index"
                            :src="require(`../assets/img/${image.image}`)"
                            alt=""
                            :style="`top: ${image.top}; left: ${image.left}`"
                        />
                    </div>
                </div>
            </div>
            <!-- Section Control -->
            <div class="ls-carousel__button-side d-none d-lg-block">
                <i @click="slidePrev" class="fas fa-chevron-circle-left"></i>
                <i @click="slideNext" class="fas fa-chevron-circle-right"></i>
            </div>
            <div class="ls-carousel__button-center">
                <i class="fas fa-circle" @click="counter = 0"></i>
                <i class="fas fa-circle" @click="counter = 1"></i>
                <i class="fas fa-circle" @click="counter = 2"></i>
            </div>
        </div>
    </div>
</template>

<script>
import slide from "../assets/data/Carousel";

export default {
    name: "Carousel",
    data() {
        return {
            slide,
            counter: 0,
        };
    },
    mounted() {
        setInterval(() => {
            this.slideNext();
        }, 40000); //! Sitsemare il tempo
    },
    methods: {
        slideNext() {
            this.counter++;
            if (this.counter == this.slide.length) {
                this.counter = 0;
            }
        },
        slidePrev() {
            this.counter--;
            if (this.counter == -1) {
                this.counter = this.slide.length - 1;
            }
        },
    },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/vars.scss";

.ls-carousel {
    position: relative;
    overflow: hidden;
    .container {
        width: 80%;
        height: 90%;
        position: relative;
        .row {
            height: 100%;
        }
    }
}

/* Section Left and right */
.ls-carousel__text {
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    h2 {
        font-size: 80px;
        font-weight: 400;
    }
    p {
        color: $color-secondary;
    }
}

.ls-carousel__image {
    position: relative;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    .ls-carousel__image-absolute {
        img {
            position: absolute;
        }
    }
}

/* Button Control */
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

.ls-carousel__button-center {
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    .fas {
        color: #e1c0b0;
        font-size: 10px;
        padding: 10px;
        cursor: pointer;
    }
}

@media (min-width: 992px) {
    .ls-carousel {
        height: 600px;
    }
}
</style>
