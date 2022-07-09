<template>
    <div class="top top__hide" id="top" v-on:click="toTop">
        <img src="../assets/goToTop.svg" alt="Top" class="top__img">
    </div>
</template>

<script>
export default {
    name: "Top",
    methods: {
        toTop() {
            document.body.scrollTop = 0;
            document.documentElement.scrollTop = 0;
        },

        checkScroll() {
            let topBtn = document.getElementById("top");

            if (document.body.scrollTop > 20 || document.documentElement.scrollTop > 20) {
                topBtn.classList.remove("top__hide");
            }
            else {
                topBtn.classList.add("top__hide");
            }
        }
    },
    mounted() {
        window.addEventListener("scroll", () => this.checkScroll());
    }
}
</script>

<style lang="scss">
.top {
    position: fixed;
    z-index: 2;

    bottom: 2rem;
    right: 2rem;

    width: 4rem;
    height: 4rem;

    display: flex;
    justify-content: center;
    align-items: center;

    border-radius: 50%;
    background-color: var(--color-green);

    transition: opacity 0.2s ease-in-out;
    -webkit-transition: opacity 0.2s ease-in-out;
    -moz-transition: opacity 0.2s ease-in-out;
    -ms-transition: opacity 0.2s ease-in-out;
    -o-transition: opacity 0.2s ease-in-out;

    box-shadow: rgba(50, 50, 93, 0.25) 0px 13px 27px -5px, rgba(0, 0, 0, 0.3) 0px 8px 16px -8px;

    cursor: pointer;

    &__img {
        filter: invert(1);
        width: 3rem;
        height: 3rem;
    }

    &__hide {
        opacity: 0;
    }
}
</style>