<template>
    <div class="footer">
        <div class="footer__wave"></div>
        <div class="footer__content">
            <div class="footer__top">
                <div class="footer__logo" v-on:click="toTop">
                    <img src="../assets/logo.png" alt="Logo" class="footer__logo__img">
                    <p class="footer__logo__text">Solitude</p>
                </div>

                <div class="footer__top__nav">
                    <a href="#products" class="footer__top__nav__text">Products</a>
                    <a href="#company" class="footer__top__nav__text">Company</a>
                    <a href="#pricing" class="footer__top__nav__text">Pricing</a>
                </div>
            </div>

            <div class="footer__middle">
                <p class="footer__middle__text">Start Creating Your Dreams Sooner</p>
            </div>

            <div class="footer__bottom">
                <p class="footer__bottom__text">© 2022 Ben Webster - Solitude is a mock website.</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Footer",
    methods: {
        toTop() {
            document.body.scrollTop = 0;
            document.documentElement.scrollTop = 0;
        },
    }
}
</script>

<style lang="scss">
.footer {
    width: 100%;
    height: 22rem;

    display: flex;
    justify-content: center;

    &__wave {
        background-size: cover;
        background-repeat: no-repeat;

        width: 100%;
        aspect-ratio: 960/100;
        background-image: url(../assets/waves.svg);
    }

    &__logo {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 13rem;

        margin-left: var(--footer-padding);

        font-weight: 600;

        cursor: pointer;


        &__img {
            width: 3rem;
            height: 3rem;
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

    &__content {
        width: 95%;
        height: 18rem;

        border-radius: 10px;
        box-shadow: rgba(50, 50, 93, 0.25) 0px 13px 27px -5px, rgba(0, 0, 0, 0.3) 0px 8px 16px -8px;
        background-color: white;

        display: flex;
        flex-direction: column;
        justify-content: space-around;

        position: absolute;
    }

    &__top {
        display: flex;
        justify-content: space-between;
        align-items: center;

        height: 5rem;
        width: 100%;

        &__nav {
            margin-right: var(--footer-padding);
            width: 20rem;

            &__text {
                transition: 200ms;
                text-decoration: none;
                color: black;
                font-size: 1.2rem;
                font-weight: 600;

                &:hover {
                    transition: 200ms;
                    color: var(--color-green);
                }
            }

            display: flex;
            justify-content: space-between;
            align-items: center;
        }
    }

    &__middle {
        font-size: 2rem;
        font-weight: 800;

        width: 100%;
        height: 5rem;

        display: flex;
        align-items: center;

        &__text {
            margin-left: var(--footer-padding);
            background: var(--color-green);
            background: linear-gradient(125deg, var(--color-green) 0%, var(--color-blue) 100%);

            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;

            width: 20rem;
        }
    }

    &__bottom {
        margin-left: var(--footer-padding);
        height: 5rem;

        display: flex;
        align-items: flex-end;
        width: 25rem;
        margin-bottom: 1rem;
    }
}

@media screen and (max-width: 550px) {
    :root {
        --footer-padding: 2rem;
    }

    .footer {
        &__top__nav {
            width: 15rem;

            &__text {
                font-size: 1rem;
            }
        }
    }
}

@media screen and (max-width: 450px) {
    .footer {
        &__middle__text {
            font-size: 1.6rem;
        }

        &__top__nav {
            flex-direction: column;
            width: fit-content;
            height: 7rem;
            margin-top: 4.5rem;
        }

        &__bottom {
            width: 20rem;
        }
    }
}
</style>