<template>
    <div :class="peaksUp ? 'peaks-up' : 'peaks-down'" class="peaks"></div>
</template>

<script>
export default {
    name: "Peaks",
    props: {
        peaksUp: Boolean
    }
}
</script>

<style lang="scss">

.peaks {
    background-size: cover;
    background-repeat: no-repeat;

    width: 100%;
    aspect-ratio: 960/100;
}
.peaks-up {
    background-image: url(../assets/peaks.svg);
}

.peaks-down {
    background-image: url(../assets/peaks2.svg);
}

@media screen and (max-width: 1500px) {
    .peaks {
        height: 17rem;
    }
}

@media screen and (max-width: 1350px) {
    .peaks {
        height: 19rem;
    }
}
</style>