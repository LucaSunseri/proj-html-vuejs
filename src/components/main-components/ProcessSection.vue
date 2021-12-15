<template>
    <div class="container">
        <h2 class="ls-title">
            Working <span class="ls-title__italic">process</span>
        </h2>
        <div class="ls-content">
            <div class="row row-cols-1 row-cols-lg-4 text-center">
                <div class="col" v-for="item in items" :key="item.id">
                    <div class="ls-cirlce">
                        <i
                            :class="item.awesome"
                            :style="`color: ${item.color}`"
                        ></i>
                    </div>
                    <h4>{{ item.text.title }}</h4>
                    <p>{{ item.text.sub }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import items from "../../assets/data/Process";

export default {
    name: "ProcessSection",
    data() {
        return {
            items,
        };
    },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

.ls-content {
    margin: 70px 0;
    .col {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    .ls-cirlce {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 160px;
        height: 160px;
        border-radius: 50%;
        background-color: #faf7f1;
        i {
            font-size: 50px;
        }
    }
    h4 {
        margin: 15px 0;
    }
    p {
        color: $color-secondary;
    }
}

@media (min-width: 992px) {
    .ls-content {
        background-image: url(../../assets/svg/line.svg);
        background-position: top;
        background-position: left 4.8rem top 0;
        background-repeat: no-repeat;
    }
}
</style>
