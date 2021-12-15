<template>
    <div class="contact-section">
        <div class="container">
            <h2 class="ls-title">
                Want to work with us? Send us
                <span class="ls-title__italic">a message!</span>
            </h2>
            <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
                eiusmod tempor incididunt ut labore et dolore. Ut enim ad minim
                veniam, quis nostrud exercitation ullamco laboris nisi ut
                aliquip ex ea commo.
            </p>
            <div class="ls-button text-center">
                <span class="ls-button-text">Contact</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Contact",
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

.contact-section {
    background-image: url(../../assets/img/h-2-background-1.jpg);
    background-repeat: no-repeat;
    background-position: center;
    padding: 10% 0;
    p {
        font-size: 20px;
        color: $color-secondary;
        text-align: center;
    }
    .ls-button-text {
        background-color: #d8f0e3;
        padding: 20px 80px;
        margin-top: 30px;
    }
}
</style>
