<template>
    <div class="ls-header">
        <!-- Header left with LOGO  -->
        <div class="ls-header__left">
            <img src="../assets/img/logo-sidearea-1.png" alt="Logo Maree" />
        </div>

        <!-- MENU DESKTOP  -->
        <div class="ls-menu-desktop d-none d-lg-block">
            <div class="ls-header__right">
                <ul>
                    <li v-for="(menu, index) in menu" :key="menu.id">
                        <a @click="isActive = index" href="#"
                            ><span :class="{ ls_active: isActive == index }">{{
                                menu.item
                            }}</span></a
                        >
                    </li>
                </ul>
                <!-- Header right with MENU  -->
                <div class="ls-header__right-button">
                    <img
                        src="../assets/svg/svg-button-hader.svg"
                        alt="Button"
                    />
                </div>
            </div>
        </div>

        <!-- MENU MOBILE  -->
        <div class="ls-menu-mobile d-lg-none">
            <!-- Header right with MENU  -->
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
            isActive: 0,
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

.ls-header__left {
    display: flex;
    justify-content: center;
    align-items: center;
    img {
        width: 90%;
        cursor: pointer;
    }
}

.ls-header__right {
    display: flex;
    justify-content: center;
    align-items: center;
    ul {
        list-style: none;
        margin: 0;
        padding: 0;
        li {
            display: inline-block;
            a {
                display: inline-block;
                text-decoration: none;
                color: black;
                letter-spacing: 0.2rem;
                padding: 0 20px;
                text-transform: uppercase;
                &:hover span {
                    box-shadow: inset 0 -6px 0 #f0cebe;
                }
                span {
                    box-shadow: inset 0 -6px 0 #fff;
                    transition: all 0.5s linear;
                }
                span.ls_active {
                    box-shadow: inset 0 -6px 0 #f0cebe;
                }
            }
        }
    }
    .ls-header__right-button {
        display: flex;
        align-items: center;
        margin-left: 25px;
        cursor: pointer;
    }
}
</style>
