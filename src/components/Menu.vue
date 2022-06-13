<template>
    <ul class="menu align-center expanded text-center SMN_effect-67">
        <li v-for="menuItem in menuList">
            <router-link :to="menuItem.url" class="menuLink" :data-hover="menuItem.title">
                {{ menuItem.title }}
            </router-link>
        </li>
    </ul>
</template>

<script>
    import {defineComponent} from "@vue/runtime-core";

    export default defineComponent({
        name: "Menu",
        setup() {
            const menuList = [
                {
                    title: "Профиль",
                    url: "/profile"
                },
                {
                    title: "Игроки",
                    url: "/gamers"
                },
                {
                    title: "Навыки",
                    url: "/skills"
                },
                {
                    title: "Помощь",
                    url: "/support"
                }
            ];
            return {
                menuList
            }
        }
    })
</script>

<style scoped>
    *,
    *:after,
    *:before {
        -webkit-box-sizing: border-box;
        -moz-box-sizing: border-box;
        box-sizing: border-box;
    }

    a:hover,
    a:focus {
        outline: none;
    }





    /*----*/

    h3 {
        color: #fff;
        font-weight: bold;
        margin: 0 0 50px 0;
        position: relative;
        padding: 0 0 5px 0;
    }

    h3:before {
        content: "";
        background: rgba(255, 255, 255, 0.1);
        bottom: -4px;
        width: 25%;
        height: 1px;
        left: 0;
        position: absolute;
    }

    .back {
        padding: 50px 0 150px 0;
    }
    body {
        background: #435a6b;
    }

    .copyright ,
    .copyright *{
        color: #fff;
        text-decoration: underline;
        font-size: 15pt;
    }

    /*
    -----------------
    common style
    -----------------
    */

    .menu {
        display: flex;
        flex-direction: column;
        gap: 15px;
        list-style-type: none;
        width: fit-content;
        margin: auto;
        padding: 0;
    }

    .menu li {
        margin: auto;
    }

    .menu .menuLink {
        display: flex;
        color: rgba(255, 255, 255, 0.8);

        font-size: 17pt;
        font-weight: 400;
        /**/
        position: relative;
        text-decoration: none;
        text-transform: uppercase;
    }
    /*
---------------------------------------
hover effect 67
---------------------------------------
*/
    .SMN_effect-67 .menuLink {
        position: relative;
    }
    .SMN_effect-67 .menuLink:after {
        content: attr(data-hover);
        position: absolute;
        left: 2px;
        text-shadow: -1px 0 red;
        top: 0;
        color: #fff;
        background: transparent;
        overflow: hidden;
        clip: rect(0, 900px, 0, 0);

    }
    .SMN_effect-67 .menuLink:before {
        content: attr(data-hover);
        position: absolute;
        left: -2px;
        text-shadow: 1px 0 blue;
        top: 0;
        color: #fff;
        background: transparent;
        overflow: hidden;
        clip: rect(0, 900px, 0, 0);

    }
    .SMN_effect-67 .menuLink:hover:before {
        animation: noise-anim-2 3s infinite linear alternate-reverse;
    }
    .SMN_effect-67 .menuLink:hover:after {
        animation: noise-anim 2s infinite linear alternate-reverse;
    }
    @keyframes noise-anim {
        0% {clip: rect(12px, 9999px, 45px, 0);}
        5% {clip: rect(83px, 9999px, 35px, 0);}
        10% {clip: rect(32px, 9999px, 20px, 0);}
        15% {clip: rect(38px, 9999px, 37px, 0);}
        20% {clip: rect(2px, 9999px, 82px, 0);}
        25% {clip: rect(72px, 9999px, 52px, 0);}
        30% {clip: rect(42px, 9999px, 86px, 0);}
        35% {clip: rect(78px, 9999px, 17px, 0);}
        40% {clip: rect(75px, 9999px, 99px, 0);}
        45% {clip: rect(91px, 9999px, 39px, 0);}
        50% {clip: rect(83px, 9999px, 13px, 0);}
        55% {clip: rect(36px, 9999px, 88px, 0);}
        60% {clip: rect(38px, 9999px, 50px, 0);}
        65% {clip: rect(39px, 9999px, 58px, 0);}
        70% {clip: rect(15px, 9999px, 75px, 0);}
        75% {clip: rect(69px, 9999px, 45px, 0);}
        80% {clip: rect(10px, 9999px, 30px, 0);}
        85% {clip: rect(99px, 9999px, 3px, 0);}
        90% {clip: rect(3px, 9999px, 9px, 0);}
        95% {clip: rect(42px, 9999px, 67px, 0);}
        100% {clip: rect(28px, 9999px, 61px, 0);}
    }
    @keyframes noise-anim-2 {
        0% {clip: rect(55px, 9999px, 11px, 0);}
        5% {clip: rect(53px, 9999px, 93px, 0);}
        10% {clip: rect(22px, 9999px, 87px, 0);}
        15% {clip: rect(16px, 9999px, 72px, 0);}
        20% {clip: rect(16px, 9999px, 34px, 0);}
        25% {clip: rect(24px, 9999px, 48px, 0);}
        30% {clip: rect(16px, 9999px, 44px, 0);}
        35% {clip: rect(24px, 9999px, 32px, 0);}
        40% {clip: rect(54px, 9999px, 55px, 0);}
        45% {clip: rect(61px, 9999px, 61px, 0);}
        50% {clip: rect(38px, 9999px, 62px, 0);}
        55% {clip: rect(16px, 9999px, 31px, 0);}
        60% {clip: rect(63px, 9999px, 86px, 0);}
        65% {clip: rect(91px, 9999px, 27px, 0);}
        70% {clip: rect(6px, 9999px, 1px, 0);}
        75% {clip: rect(13px, 9999px, 52px, 0);}
        80% {clip: rect(3px, 9999px, 81px, 0);}
        85% {clip: rect(62px, 9999px, 96px, 0);}
        90% {clip: rect(1px, 9999px, 26px, 0);}
        95% {clip: rect(41px, 9999px, 83px, 0);}
        100% {clip: rect(6px, 9999px, 9px, 0);}
    }
</style>