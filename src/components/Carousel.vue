<template>
    <div class="ls-carousel">
        <div class="container">
            <div class="row">
                <div class="col-12 col-md-6 ciao">
                    <h2>Devotion that never ends</h2>
                    <p>
                        Neque porro quisqua, est, qui dolorem ipsum quia dolor
                        sit amet, consectetur, adipisci velit, sed quia non
                        numquam eius modi.
                    </p>
                    <div class="ls-button">
                        <span class="ls-button-text">Read more</span>
                    </div>
                </div>
                <div class="col-12 col-md-6">
                    <img src="../assets/img/h-2-slider-img-11.png" alt="" />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Carousel",
};
</script>

<style lang="scss" scoped>
.ciao {
    display: flex;
    flex-direction: column;
    justify-content: center;
}
img {
    width: 100%;
}
</style>
