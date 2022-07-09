<template>
    <div class="logo" v-on:click="home">
        <img src="../assets/logo.png" alt="Logo" class="logo__img">
        <p class="logo__text">Solitude</p>
    </div>
</template>

<script>
export default {
    name: "Logo",
    methods: {
        home() {
            window.location.href = "/";
        }
    }
}
</script>

<style lang="scss">
$logo-size: 3rem;

.logo {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 13rem;

    position: absolute;
    left: var(--logo-sideSpacing);

    font-weight: 600;

    cursor: pointer;
    

    &__img {
        width: $logo-size;
        height: $logo-size;
    }

    &__text {
        transition: 200ms;
        font-size: 2.5rem;
        color: rgb(36, 36, 36);
    }

    &:hover &__text {
        transition: 200ms;
        color: var(--color-green);
    }
}
</style>