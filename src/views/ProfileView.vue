<template>
    <ProfileHeader class="header" />
</template>

<script>
    import ProfileHeader from '../components/ProfileHeader.vue'
    export default {
        name: "ProfileView",
        components: {
            ProfileHeader
        }
    }
</script>

<style scoped>
    .header {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        background: rgba(23, 52, 118, 0.3);
    }
</style>