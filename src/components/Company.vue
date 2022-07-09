<template>
    <div class="company" id="company">
        <Peaks :peaksUp="false"></Peaks>

        <div class="company__content">
            <div class="company__content__top">
                <p class="company__content__top__title">Company</p>
                <p class="company__content__top__about">Here at Solitude, our company is like family.</p>
                <p class="company__content__top__extra">You can start your career today!</p>
            </div>

            <div class="company__content__middle">
                <div class="company__content__middle__card left-margin">
                    <img src="../assets/person.svg" alt="People Image" class="company__content__middle__card__img">
                    <p class="company__content__middle__card__text"><span class="company__content__middle__card__text-extra">750</span> Employees</p>
                </div>

                <div class="company__content__middle__card">
                    <img src="../assets/company.svg" alt="People Image" class="company__content__middle__card__img">
                    <p class="company__content__middle__card__text"><span class="company__content__middle__card__text-extra">50+</span> Fortune 500 Clients</p>
                </div>

                <div class="company__content__middle__card right-margin">
                    <img src="../assets/global.svg" alt="Earth Image" class="company__content__middle__card__img">
                    <p class="company__content__middle__card__text"><span class="company__content__middle__card__text-extra">70+</span> Countries</p>
                </div>
            </div>

            <div class="company__content__bottom">
                <button class="company__content__bottom__btn">Start Your Career Today</button>
            </div>
        </div>
    </div>
</template>

<script>
import Peaks from './Peaks.vue';
export default {
    name: "Company",
    components: {
        Peaks 
    }
}
</script>

<style lang="scss">
.company {
    width: 100%;
    height: 55rem;

    &__content {
        display: flex;
        flex-direction: column;
        align-items: center;

        width: 100%;
        height: 100%;

        &__top {
            width: 100%;

            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;

            text-align: center;

            &__title {
                color: var(--color-green);
                font-weight: 600;
                font-size: 1.4rem;
            }

            &__about {
                font-size: 2.5rem;
                font-weight: 600;
                margin: 1rem 2rem 1rem 2rem;
            }

            &__extra {
                font-size: 1.3rem;
                font-weight: 600;
                color: rgb(100, 100, 100);
            }
        }

        &__middle {
            display: flex;
            justify-content: space-around;
            align-items: center;

            width: 100%;
            height: 25rem;

            &__card {
                width: 30rem;
                height: 20rem;
                border-radius: 5px;

                display: flex;
                flex-direction: column;
                align-items: center;
                justify-content: space-around;

                &__img {
                    width: 13rem;
                    height: 13rem;

                    filter: var(--color-blue-filter);
                }

                &__text {
                    font-size: 2rem;
                    font-weight: 600;

                    text-align: center;

                    &-extra {
                        font-size: 2.2rem;
                        font-weight: 800;
                        color: var(--color-green);
                    }
                }
            }
        }

        &__bottom {
            width: 100%;
            height: 5rem;

            display: flex;
            justify-content: center;
            align-items: center;

            &__btn {
                transition: 200ms;
                display: flex;
                justify-content: space-around;
                align-items: center;
                width: 14rem;

                border-radius: 10px;

                margin-top: 5rem;

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
    }
}

.left-margin {
    margin-left: 1rem;
}

.right-margin {
    margin-right: 1rem;
}

@media screen and (max-width: 1500px) {
    .company {
        height: 60rem;
    }
}

@media screen and (max-width: 650px) {
    .company {
        height: 100rem;

        &__content__middle {
            flex-direction: column;
            height: fit-content;

            &__card {
                width: 23rem;
            }
        }
    }
}
</style>