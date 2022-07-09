<template>
    <div class="header">
        <Logo/>

        <div class="header__navbar">
            <a class="header__navbar__text" href="#products">Products</a>
            <a class="header__navbar__text" href="#company">Company</a>
            <a class="header__navbar__text" href="#pricing">Pricing</a>
        </div>

        <div class="header__signup">
            <p class="header__signup__text">Sign Up</p>
        </div>
    </div>
</template>

<script>
import Logo from './Logo.vue';
export default {
    name: "Header",
    components: {
        Logo
    },
    methods: {
        home() {
            window.location.href = "/";
        }
    }
}
</script>

<style lang="scss">
$logo-size: 3rem;

.header {
    display: flex;
    align-items: center;

    width: 100%;
    height: 7rem;

    font-weight: 600;

    &__title {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 13rem;

        position: absolute;
        left: var(--logo-sideSpacing);

        cursor: pointer;
        

        &__img {
            width: $logo-size;
            height: $logo-size;
        }

        &__text {
            transition: 200ms;
            font-size: 2.5rem;
        }

        &:hover &__text {
            transition: 200ms;
            color: var(--color-green);
        }
    }

    &__navbar {
        display: flex;
        justify-content: space-between;
        align-items: center;

        width: 22rem;
        height: 4rem;

        position: absolute;
        left: calc(50% - 24rem / 2);

        &__text {
            transition: 200ms;
            text-decoration: none;
            color: rgb(36, 36, 36);
            font-size: 1.1rem;

            height: 100%;
            width: 7rem;
            
            display: flex;
            align-items: center;
            justify-content: center;

            &:hover {
                transition: 200ms;
                color: var(--color-green);
            }
        }
    }

    &__signup {
        transition: 200ms;
        display: flex;
        justify-content: space-around;
        align-items: center;

        position: absolute;
        width: 5rem;
        right: var(--logo-sideSpacing);

        border-radius: 10px;

        cursor: pointer;

        padding: 0.7rem 0.5rem 0.7rem 0.5rem;
        background-color: var(--color-blue);
        color: white;

        &:hover {
            transition: 200ms;
            background-color: var(--color-green);
        }
    }
}

@media screen and (max-width: 1300px) {
    .header__navbar {
        display: none;
    }
}

@media screen and (max-width: 350px) {
    :root {
        --logo-sideSpacing: 3rem;
    }
}
</style>