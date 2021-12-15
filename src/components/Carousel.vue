<template>
    <div class="ls-carousel">
        <!-- SECTION CONTENT -->
        <div
            class="ls-carousel__content animate__animated animate__slideInRight"
            v-for="(slide, index) in slide"
            :key="slide.id"
            :class="{ ls_active: counter == index }"
        >
            <div class="container">
                <div class="row">
                    <!-- Section Content Text -->
                    <div class="col-12 col-lg-6">
                        <div class="ls-carousel__text">
                            <h2>
                                {{ slide.text.title }}
                                <span class="ls-title__italic">{{
                                    slide.text.italic
                                }}</span>
                            </h2>
                            <p class="d-none d-md-block">{{ slide.text.p }}</p>
                            <div class="ls-button">
                                <span class="ls-button-text">Read more</span>
                            </div>
                        </div>
                    </div>
                    <!-- Section Content Image -->
                    <div class="col-12 col-lg-6">
                        <div class="ls-carousel__image">
                            <img
                                v-for="(image, key) in slide.imageCenter"
                                :key="key"
                                :style="`width: ${image.width}`"
                                :src="require(`../assets/img/${image.image}`)"
                                alt=""
                                class="animate__animated animate__fadeInUp"
                            />
                            <div class="ls-carousel__image-absolute">
                                <img
                                    v-for="(
                                        image, index
                                    ) in slide.imageAbsolute"
                                    :key="index"
                                    :style="`top: ${image.top}; left: ${image.left}`"
                                    :src="
                                        require(`../assets/img/${image.image}`)
                                    "
                                    alt=""
                                />
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- SECTION CONTROL -->
        <div class="ls-carousel__control">
            <!-- Button Side -->
            <div class="ls-carousel__control-button-side d-none d-lg-block">
                <i @click="slidePrev" class="fas fa-chevron-circle-left"></i>
                <i @click="slideNext" class="fas fa-chevron-circle-right"></i>
            </div>
            <!-- Button Center -->
            <div class="ls-carousel__control-button-center">
                <i
                    v-for="(item, index) in 3"
                    :key="index"
                    class="fas fa-circle"
                    :class="{ ls_active: counter == index }"
                    @click="counter = index"
                ></i>
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
        }, 5000);
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
@import "~animate.css";

.ls-carousel {
    position: relative;
    overflow: hidden;
    margin-bottom: 3rem;
}

.ls-carousel__content {
    display: none;
    height: 100%;
    .container {
        width: 80%;
        height: 95%;
    }
    .row {
        height: 100%;
        .col {
            height: 100%;
        }
    }
}

.ls-carousel__content.ls_active {
    display: block;
}

/* Section Left and right */
.ls-carousel__text {
    position: relative;
    z-index: 200;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    h2 {
        font-size: 80px;
        font-weight: 400;
    }
    p {
        color: $color-secondary;
    }
    .ls-button-text {
        border: 3px solid #e1c0b0;
        padding: 20px 40px;
        margin-top: 15px;
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
            z-index: 100;
        }
    }
}

/* Button Control */
.ls-carousel__control-button-side {
    .fas {
        position: absolute;
        z-index: 900;
        top: 50%;
        transform: translateY(-50%);
        font-size: 30px;
        color: #e1c0b0;
        cursor: pointer;
    }
    .fa-chevron-circle-left {
        left: 50px;
    }
    .fa-chevron-circle-right {
        right: 50px;
    }
}

.ls-carousel__control-button-center {
    position: absolute;
    z-index: 900;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    .fas {
        color: #e1c0b0;
        font-size: 8px;
        padding: 10px;
        cursor: pointer;
    }
    .fas.ls_active {
        transform: scale(1.5);
    }
}

@media (min-width: 992px) {
    .ls-carousel {
        height: 600px;
    }
}
</style>
