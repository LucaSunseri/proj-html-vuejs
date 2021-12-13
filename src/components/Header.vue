<template>
    <div class="ls-header">
        <div class="ls-header__left">
            <img src="../assets/img/logo-sidearea-1.png" alt="Logo Maree" />
        </div>

        <div class="ls-menu-desktop d-none d-lg-block">
            <div class="ls-header__right">
                <ul>
                    <li v-for="menu in menu" :key="menu.id">
                        <a href="#">{{ menu.item }}</a>
                    </li>
                </ul>
                <div class="ls-header__right-button">
                    <img
                        src="../assets/svg/svg-button-hader.svg"
                        alt="Button"
                    />
                </div>
            </div>
        </div>

        <div class="ls-menu-mobile d-lg-none">
            <div class="ls-header__right">
                <div class="ls-header__right-button">
                    <img
                        src="../assets/svg/svg-button-hader.svg"
                        alt="Button"
                    />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import menu from "../assets/data/Menu.js";

export default {
    name: "Header",
    data() {
        return {
            menu,
        };
    },
};
</script>

<style lang="scss" scoped>
.ls-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 80px;
    line-height: 80px;
    padding: 0 40px;
    font-size: 14px;
    font-weight: bold;
}

.ls-header__right {
    display: flex;
    ul {
        list-style: none;
        margin: 0;
        padding: 0;
        li {
            display: inline-block;
            padding: 0 25px;
            a {
                display: inline-block;
                text-decoration: none;
                color: black;
                text-transform: uppercase;
            }
        }
    }
    .ls-header__right-button {
        display: flex;
        align-items: center;
        margin-left: 25px;
    }
}
</style>
