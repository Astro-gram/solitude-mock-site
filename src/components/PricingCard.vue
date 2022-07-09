<template>
    <div class="pricingCard">
        <div class="pricingCard__content">
            <p class="pricingCard__content__title">{{ unit }} Plan</p>
            <div class="pricingCard__content__price">
                <p class="pricingCard__content__price-number">${{ cost }}</p>
                <p class="pricingCard__content__price-text" v-if="!hidePerUnit">Per {{ unit }}</p>
            </div>

            <div class="pricingCard__content__includes">
                <p class="pricingCard__content__includes-include"><span class="green">✓</span> Full Access to our suite of products</p>
                <p class="pricingCard__content__includes-include"><span class="green">✓</span> Access to over 10k design templates</p>
                <p class="pricingCard__content__includes-include"><span class="green">✓</span> Community of over 100k designer</p>
                <p class="pricingCard__content__includes-include"><span class="green">✓</span> Regular updates and bug fixes</p>
            </div>

            <div class="pricingCard__content__btn-container">
                <button class="pricingCard__content__btn">Get Started</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "PricingCard",
    props: {
        unit: String,
        cost: String,
        costPerMonth: String,
        hidePerUnit: Boolean,
    }
}
</script>

<style lang="scss">
.pricingCard {
    display: flex;
    justify-content: center;
    align-items: center;

    color: white;

    &__content {
        width: 90%;
        height: 90%;

        background-color: var(--color-blue-light);
        border-radius: 5px;
        border: 2px solid white;

        display: flex;
        flex-direction: column;

        &__includes {
            display: flex;
            flex-direction: column;
            align-items: center;

            &__title {
                color: white;
                font-size: 2rem;
                font-weight: 600;
                margin-bottom: 1rem;
            }

            &-include {
                color: white;
                font-size: 1.2rem;
                font-weight: 600;
                text-align: center;
            }
        }
    

        &__btn {
            transition: 200ms;
            background-color: var(--color-blue);

            width: fit-content;
            border: 2px solid white;
            border-radius: 5px;
            padding: 0.7rem;

            font-size: 1.2rem;
            font-weight: 600;

            color: white;

            &:hover {
                transition: 200ms;
                background-color: var(--color-blue-light);
                cursor: pointer;
            }

            &-container {
                display: flex;
                justify-content: center;
                align-items: center;

                width: 100%;
                height: 6rem;
            }
        }

        &__price {
            height: 7rem;

            display: flex;
            align-items: center;
            margin-left: 2rem;

            &-number {
                font-size: 4rem;
                font-weight: 800;
            }

            &-text {
                font-size: 1.2rem;
                font-weight: 600;
                margin-left: 1rem;
            }
        }

        &__title {
            transition: 200ms;
            width: fit-content;

            background-color: hsla(0, 0%, 100%, 0.3);

            padding: 0.3rem 0.7rem 0.3rem 0.7rem;
            border-radius: 50px;

            font-weight: 600;
            font-size: 1.2rem;
            text-align: center;

            margin: 0.5rem 0rem 0rem 0.5rem;
        }
    }
}

.green {
    color: var(--color-green);
    margin-right: 0.5rem;
}

@media screen and (max-width: 850px) {
    .pricingCard__content__includes {
        &-include {
            width: 90%;
        }
    }
}
</style>