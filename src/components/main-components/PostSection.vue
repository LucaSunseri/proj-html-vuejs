<template>
    <div class="container">
        <div class="row row-cols-1 row-cols-md-2 row-cols-lg-3">
            <div class="col ls-box" v-for="post in posts" :key="post.id">
                <!-- Box TOP containing image -->
                <div class="ls-box__top">
                    <div class="ls-box__top-image">
                        <img
                            :src="require(`../../assets/img/${post.image}`)"
                            :alt="post.alt"
                        />
                    </div>

                    <!-- Box in posiction absolute containing date -->
                    <div class="ls-box__top-date">
                        <div class="ls-day">
                            <span>{{ post.date.day }}</span>
                        </div>
                        <div class="ls-m-and-y">
                            <span>{{ post.date.mAndY }}</span>
                        </div>
                    </div>
                </div>

                <!-- Box BOTTOM containing text -->
                <div class="ls-box__bottom">
                    <h3>
                        <a href="#">{{ post.text.title }}</a>
                    </h3>
                    <p class="ls-italic">By {{ post.text.author }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import posts from "../../assets/data/Post";

export default {
    name: "PostSection",
    data() {
        return {
            posts,
        };
    },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

.ls-box {
    margin-bottom: 30px;
}

.ls-box__top {
    position: relative;
    cursor: pointer;
    .ls-box__top-image {
        overflow: hidden;
        img {
            width: 100%;
            transform: scale(1);
            transition: all 0.8s ease-in-out;
        }
        &:hover img {
            transform: scale(1.1);
        }
    }
}

.ls-box__top-date {
    position: absolute;
    top: -20px;
    left: 15px;
    .ls-day {
        font-size: 35px;
        font-weight: bold;
        font-family: $font-secondary;
        background-color: #c0e1cf;
        text-align: center;
        line-height: 45px;
    }
    .ls-m-and-y {
        font-size: 14px;
        padding: 0 5px 12px 5px;
        background-color: #f3d0c7;
        clip-path: polygon(0 0, 100% 0, 100% 100%, 50% 70%, 0 100%);
    }
}

.ls-box__bottom {
    margin-top: 15px;
    a {
        text-decoration: none;
        color: black;
        font-weight: 300;
    }
}
</style>
