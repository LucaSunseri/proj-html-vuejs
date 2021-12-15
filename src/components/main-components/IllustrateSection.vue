<template>
    <div>
        <div class="ls-box">
            <div class="row row-cols-1 row-cols-sm-2 row-cols-md-3">
                <div class="col" v-for="item in items" :key="item.id">
                    <img
                        :src="require(`../../assets/img/${item.image}`)"
                        :alt="item.hover.title"
                    />
                    <div
                        class="ls-box__hover animate__animated animate__fadeIn"
                    >
                        <h3>{{ item.hover.title }}</h3>
                        <p>{{ item.hover.sub }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import items from "../../assets/data/Illustrate";

export default {
    name: "IllustrateSection",
    data() {
        return {
            items,
            hover: false,
        };
    },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";
@import "~animate.css";

.ls-box {
    cursor: pointer;
    .row {
        --bs-gutter-x: 0;
    }
    .col {
        position: relative;
        z-index: 400;
        &:hover .ls-box__hover {
            display: block;
        }
    }
    img {
        width: 100%;
    }
}

.ls-box__hover {
    display: none;
    position: absolute;
    z-index: 200;
    top: 50%;
    transform: translateY(-50%);
    left: 0;
    padding: 25px 30px;
    background-color: white;
    p {
        font-family: $font-secondary;
        font-style: italic;
        margin: 0;
    }
}
</style>
