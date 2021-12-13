<template>
    <div class="container">
        <div class="row row-cols-1 row-cols-md-2 row-cols-lg-3">
            <div class="col ls-box" v-for="post in posts" :key="post.id">
                <div class="ls-box__top">
                    <img
                        :src="require(`../../assets/img/${post.image}`)"
                        :alt="post.alt"
                    />
                    <div class="ls-box__top-date">
                        <div class="ls-day">
                            <span>{{ post.date.day }}</span>
                        </div>
                        <div class="ls-m-and-y">
                            <span>{{ post.date.mAndY }}</span>
                        </div>
                    </div>
                </div>
                <div class="ls-box__bottom">
                    <h3>
                        <a href="#">{{ post.text.title }}</a>
                    </h3>
                    <p>By {{ post.text.author }}</p>
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

.ls-box__top {
    position: relative;
    img {
        width: 100%;
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
    a {
        text-decoration: none;
        color: black;
    }
}
</style>
