<template>
    <div class="ls-carousel">
        <div class="container">
            <div class="row">
                <div class="col-12 col-lg-6 ciao">
                    <h2>
                        Devotion that never
                        <span class="ls-title__italic">ends</span>
                    </h2>
                    <p>
                        Neque porro quisqua, est, qui dolorem ipsum quia dolor
                        sit amet, consectetur, adipisci velit, sed quia non
                        numquam eius modi.
                    </p>
                    <div class="ls-button">
                        <span class="ls-button-text">Read more</span>
                    </div>
                </div>
                <div class="col-12 col-lg-6 ls-carousel__image">
                    <img
                        src="../assets/img/h-2-slider-img-15.png"
                        alt=""
                        style="width: 50%"
                    />
                    <img
                        src="../assets/img/h-2-slider-img-16.png"
                        alt=""
                        style="width: 50%"
                    />
                    <div class="ls-carousel__image-absolute">
                        <img
                            src="../assets/img/short-slider-rev-1-img-2.png"
                            alt=""
                            style="top: 3%; left: 3%"
                        />
                        <img
                            src="../assets/img/h-2-slider-img-12.png"
                            alt=""
                            style="top: 50%; left: -10%"
                        />
                        <img
                            src="../assets/img/h-2-slider-img-13.png"
                            alt=""
                            style="top: 80%; left: 0"
                        />
                        <img
                            src="../assets/img/h-2-slider-img-14.png"
                            alt=""
                            style="top: -10%; left: 80%"
                        />
                        <img
                            src="../assets/img/short-slider-rev-1-img-6.png"
                            alt=""
                            style="top: 15%; left: 90%"
                        />
                        <img
                            src="../assets/img/h-2-slider-img-17.png"
                            alt=""
                            style="top: 80%; left: 100%"
                        />
                    </div>
                </div>
                <div class="ls-carousel__button-side d-none d-lg-block">
                    <i class="fas fa-chevron-circle-left"></i>
                    <i class="fas fa-chevron-circle-right"></i>
                </div>
            </div>
        </div>

        <div class="ls-carousel__button-center">
            <i class="fas fa-circle"></i>
            <i class="fas fa-circle"></i>
            <i class="fas fa-circle"></i>
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
        };
    },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/vars.scss";

.ls-carousel {
    position: relative;
    padding: 100px 0;
    overflow: hidden;
    .container {
        width: 80%;
        .row {
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
    margin-top: 50px;
    .fas {
        color: #e1c0b0;
        font-size: 10px;
        padding: 10px;
        cursor: pointer;
    }
}
</style>
