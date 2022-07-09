<template>
    <div class="hero">
        <div class="hero__content">
            <div class="hero__text">
                <p class="hero__text__main">Start Creating Your Dreams Sooner</p>
                <p class="hero__text__extra">Create your mock website using our industry-leading technology.</p>
                <button class="hero__text__btn">Start Now</button>
            </div>

            <div class="hero__img-container">
                <img src="../assets/hero.png" alt="Promo" class="hero__img">
            </div>
        </div>

        <Peaks :peaksUp="true"></Peaks>
    </div>
</template>

<script>
import Peaks from './Peaks.vue';
export default {
    name: "Hero",
    components: {
        Peaks 
    }
}
</script>

<style lang="scss">
.hero {
    width: 100%;
    height: 100vh;

    display: flex;
    flex-direction: column;
    justify-content: space-between;

    &__content {
        height: 90%;
        display: flex;
        justify-content: space-around;
        align-items: center;
    }

    &__text {
        width: 40rem;
        height: 18rem;

        display: flex;
        flex-direction: column;
        justify-content: space-between;

        &__main {
            font-weight: 800;
            font-size: 4rem;

            background: var(--color-green);
            background: linear-gradient(125deg, var(--color-green) 0%, var(--color-blue) 100%);

            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        &__extra {
            font-size: 1.4rem;
            width: 25rem;
        }

        &__btn {
            transition: 200ms;
            display: flex;
            justify-content: space-around;
            align-items: center;
            width: 8rem;

            border-radius: 10px;

            cursor: pointer;

            padding: 0.7rem 0.5rem 0.7rem 0.5rem;
            background-color: var(--color-green);
            color: white;
            border: none;

            font-weight: 600;
            font-size: 1rem;

            &:hover {
                transition: 200ms;
                background-color: var(--color-blue);
            }
        }
    }

    &__img {
        aspect-ratio: 4/3;
        height: 38rem;
        border-radius: 20px;
    }
}

@media screen and (max-width: 1575px) {
    .hero {
        &__content {
            justify-content: center;
        }
    }
}

@media screen and (max-width: 1500px) {
    html {
        font-size: 90%;
    }

    .hero {
        &__img {
            height: 35rem;
        }
    }
}

@media screen and (max-width: 1350px) {
    html {
        font-size: 80%;
    }

    .hero {
        &__img {
            height: 33rem;
        }
    }
}

@media screen and (max-width: 1150px) {
    .hero {
        &__text {
            height: 17rem;
            width: 35rem;

            &__main {
                font-size: 3.5rem;
            }

            &__extra {
                font-size: 1.3rem;
            }
        }

        &__img {
            height: 30rem;
        }

        &__content {
            margin-top: 5rem;
        }
    }
}

@media screen and (max-width: 1000px) {
    html {
        font-size: 70%;
    }
}

@media screen and (max-width: 880px) {
    .hero {
        &__content {
            flex-direction: column;
            text-align: center;
            justify-content: space-around;
            padding: 2rem 0rem 2rem 0rem;
            margin-top: 0rem;
        }

        &__text {
            align-items: center;
            margin-bottom: 2rem;
            height: 28rem;

            &__main {
                font-size: 5rem;
            }

            &__extra {
                font-size: 1.7rem;
            }

            &__btn {
                width: 10rem;
                height: 3rem;
                font-size: 1.2rem;
            }
        }
    }
}

@media screen and (max-width: 500px) {
    .hero {
        &__text {
            height: 23rem;

            &__main {
                font-size: 4rem;
            }

            &__extra {
                font-size: 1.2rem;
            }
        }

        &__img {
            height: 25rem;
        }

        &__content {
            padding-bottom: 1rem;
        }
    }
}

@media screen and (max-width: 400px) {
    html {
        font-size: 60%;
    }

    .hero {

        &__text {
            margin-bottom: 4rem;
        }

        &__content {
            justify-content: left;
            margin-top: 5rem;
        }
    }
}

@media screen and (max-width: 360px) {
    .hero {
        &__img {
            height: 20rem;
        }

        &__text {
            height: 14rem;
            width: 30rem;

            &__main {
                font-size: 2.8rem;
            }

            &__extra {
                font-size: 1.1rem;
            }

            margin-bottom: 2rem;
        }

        &__content {
            margin-top: 5rem;
        }
    }
}

@media screen and (max-width: 310px) {
    .hero__text {
        width: fit-content;
    }
}
</style>