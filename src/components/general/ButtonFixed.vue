<template>
    <div
        :style="`width: ${width}; height: ${height}; bottom: ${bottom}; right: ${right}; background-color: ${background}`"
    >
        <img
            :src="require(`../../assets/svg/${image}`)"
            :alt="alt"
            :style="`width: ${widthimg}`"
        />
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
div {
    position: fixed;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    box-shadow: -2px 4px 6px -4px #000000;
}
</style>
