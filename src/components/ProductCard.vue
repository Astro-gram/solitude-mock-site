<template>
    <div class="productCard">
        <div class="productCard__content">
            <p class="productCard__content__title">{{ title }}</p>
            <p class="productCard__content__extra">{{ extra }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: "ProductCard",
    props: {
        title: String,
        extra: String,
    }
}
</script>

<style lang="scss">
.productCard {
    transition: 200ms;
    width: 100%;
    height: 8.5rem;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    border-radius: 5px;

    border: 2px solid white;

    background-color: var(--color-blue-light);

    &:hover {
        transition: 200ms;
        transform: translate(10px, -5px);
    }

    &:hover &__content__title {
        transition: 200ms;
        color: var(--color-green);
    }

    &__content {
        display: flex;
        flex-direction: column;
        justify-content: space-around;

        width: 95%;
        height: 100%;

        &__title {
            transition: 200ms;
            width: fit-content;

            background-color: hsla(0, 0%, 100%, 0.3);
            color: white;

            padding: 0.3rem 0.7rem 0.3rem 0.7rem;
            border-radius: 50px;

            font-weight: 600;
            font-size: 1.2rem;
            text-align: center;

            margin-top: 0.2rem;
        }

        &__extra {
            color: white;
            font-weight: 600;
        }
    }
}

@media screen and (max-width: 500px) {
    .productCard__content__extra {
        font-size: 1rem;
    }
}
</style>