<template>
    <header class="header-block">
        <div class="avatar-block">
            <div class="avatar"></div>
            <div class="name-block">
                <p>Denis Shmakov</p>
                <p>Front-end Developer</p>
            </div>
        </div>
        <div class="points-block">
            <p class="points">66/74 Points</p>
            <p class="level">4-s level</p>
        </div>
    </header>
</template>

<script>
    export default {
        name: "ProfileHeader"
    }
</script>

<style scoped>
    .header-block {
        padding: 16px;
    }
    .avatar-block {
        display: flex;
        flex-direction: row;
        gap: 8px;
        margin-bottom: 8px;
    }
    .avatar {
        width: 50px;
        height: 50px;
        border-radius: 50%;
        background-image: url("../assets/images/warcraft-avatar.jpg");
        background-size: cover;
        background-position: center;
    }
    .name-block {
        display: flex;
        flex-direction: column;
    }
    .points-block {
        display: flex;
        flex-direction: row;
        gap: 8px;
    }
</style>