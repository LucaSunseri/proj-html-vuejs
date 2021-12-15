<template>
    <div>
        <a href="#">
            <div
                class="ls-custom"
                :style="`width: ${width}; height: ${height}; bottom: ${bottom}; right: ${right}; background-color: ${background}`"
            >
                <img
                    :src="require(`../../assets/svg/${image}`)"
                    :alt="alt"
                    :style="`width: ${widthimg}`"
                />
            </div>
        </a>
    </div>
</template>

<script>
export default {
    name: "ButtonFixed",
    props: {
        image: String,
        alt: String,
        widthimg: String,
        background: String,
        bottom: String,
        right: String,
        width: String,
        height: String,
    },
};
</script>

<style lang="scss" scoped>
.ls-custom {
    position: fixed;
    z-index: 999;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    box-shadow: -2px 4px 6px -4px #000000;
}
</style>
