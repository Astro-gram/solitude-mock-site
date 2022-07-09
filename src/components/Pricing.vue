<template>
    <div class="pricing" id="pricing">
        <div class="pricing__wave"></div>

        <div class="pricing__content">
            <div class="pricing__content__left">
                <PricingCard :cost="'15'" :unit="'Month'" :costPerMonth="'15'"/>
                <PricingCard :cost="'39'" :unit="'Quarter'" :costPerMonth="'13'"/>
                <PricingCard :cost="'120'" :unit="'Year'" :costPerMonth="'10'" />
                <PricingCard :cost="'???'" :unit="'Custom'" :hidePerUnit="true"/>
            </div>

            <div class="pricing__content__right">
                <div class="pricing__content__right-textContainer">
                    <p class="pricing__content__right__title">Pricing</p>
                    <p class="pricing__content__right__about">Pricing built for people or business of any size</p>
                    <p class="pricing__content__right__extra">Here at Solitude we always want to be transparent about our pricing.</p>
                </div>

                <p class="pricing__content__right__text">Join designers and creators from across the globe using our cutting edge technology to develop anything they dream of.</p>

                <div></div>
            </div>
        </div>
    </div>
</template>

<script>
import PricingCard from './PricingCard.vue';
export default {
    name: "Pricing",
    components: {
        PricingCard 
    }
}
</script>

<style lang="scss">
.pricing {
    width: 100%;
    height: 75rem;
    background-color: var(--color-blue);

    display: flex;
    flex-direction: column;
    align-items: center;

    &__wave {
        background-size: cover;
        background-repeat: no-repeat;

        width: 100%;
        aspect-ratio: 960/100;
        background-image: url(../assets/Vector.svg);
    }

    &__content {
        width: 90rem;
        height: 75%;

        display: flex;
        align-items: center;
        justify-content: center;

        &__left {
            width: 65%;
            height: 100%;

            display: grid;
            grid-template-rows: auto auto;
            grid-template-columns: auto auto;
        }

        &__right {
            width: 35%;
            height: 100%;

            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-between;

            border-right: 1px solid white;

            &-textContainer {
                width: 90%;
                height: 14rem;

                display: flex;
                flex-direction: column;
                justify-content: space-between;
                font-weight: 600;
            }

            &__text {
                color: white;
                font-size: 1.8rem;
                font-weight: 600;

                width: 80%;
                text-align: center;
            }

            &__title {
                color: var(--color-yellowGreen);
                font-size: 1.4rem;
            }

            &__about {
                color: white;
                font-size: 2.5rem;
                
            }

            &__extra {
                font-size: 1.3rem;
                color: rgb(199, 199, 199);
                margin-top: 2rem;
            }
        }
    }
}

@media screen and (max-width: 1600px) {
    .pricing {
        &__content {
            width: 80rem;
        }
    }
}

@media screen and (max-width: 1100px) {
    .pricing {
        &__content {
            width: 70rem;
        }
    }
}

@media screen and (max-width: 850px) {
    .pricing {
        height: 100rem;

        &__content {
            width: 50rem;
            height: 80%;
            flex-direction: column-reverse;

            &__right {
                width: 100%;

                &__extra,
                &__about {
                    text-align: center;
                }
            }

            &__left {
                width: 100%;
                border-right: 1px solid white;

                grid-template-columns: 47% 47%;
            }
        }
    }
}

@media screen and (max-width: 600px) {
    .pricing {
        height: 130rem;

        &__content {
            width: 40rem;
            height: 90%;

            &__left {
                grid-template-columns: 100%;
            }
        }
    }
}

@media screen and (max-width: 475px) {
    .pricing {
        &__content {
            height: 95%;
            width: 30rem;
        }
    }
}

@media screen and (max-width: 325px) {
    .pricing {
        height: 150rem;

        &__content {
            width: 25rem;
        }
    }
}
</style>