<template>
    <b-row
        cols="2"
        cols-sm="4"
        class="text-center ls-position"
        style="font-size: 2.8rem"
    >
        <b-col>
            <b-icon icon="arrow-up" class="ls-bg-color p-2"></b-icon>
        </b-col>
    </b-row>
</template>

<script>
export default {
    name: "Arrow",
};
</script>

<style lang="scss" scoped>
.ls-position {
    position: fixed;
    bottom: 10px;
    right: 20px;
    cursor: pointer;
}

.ls-bg-color {
    background-color: #c0e1cf;
    color: white;
}
</style>
