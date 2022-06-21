<template>
    <ProfileHeader class="header" />
    <div class="profileMenuBlock">
        <ul class="profileMenu align-center expanded text-center SMN_effect-67">
            <li v-for="profileMenuItem in profileMenuList">
                <router-link :to="profileMenuItem.url" class="profileItem">
                    {{ profileMenuItem.title }}
                </router-link>
            </li>
        </ul>
    </div>
</template>

<script>
    import ProfileHeader from '../components/ProfileHeader.vue';
    import {defineComponent} from "@vue/runtime-core";

    export default defineComponent({
        name: "ProfileView",
        components: {
            ProfileHeader
        },
        setup() {
            const profileMenuList = [
                {
                    title: "навыки в работе",
                    url: "/profile/skillInProgress"
                },
                {
                    title: "освенные навыки",
                    url: "/profile/skillDone"
                },
                {
                    title: "достижения",
                    url: "/profile/achievements"
                }
            ];
            return {
                profileMenuList
            }
        }
    })
</script>

<style scoped>
    .header {
        top: 0;
        left: 0;
        width: 100%;
        background: rgba(23, 52, 118, 0.3);
    }
    .profileMenuBlock {
        display: flex;
        width: fit-content;
        background: rgba(0, 0, 0, 0.4);
        padding: 20px;
        border-right: 2px solid white;
        height: 100%;
    }
    .profileMenu {
        display: flex;
        flex-direction: column;
        gap: 15px;
        list-style-type: none;
        width: fit-content;
        padding: 0;
    }
    .profileMenu .profileItem {
        display: flex;
        color: rgba(255, 255, 255, 0.8);

        font-size: 17pt;
        font-weight: 400;
        /**/
        position: relative;
        text-decoration: none;
        text-transform: uppercase;
    }
</style>