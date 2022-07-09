<template>
    <div class="home">
		<Header/>
		<Hero/>
		<Products/>
        <Company/>
        <Pricing/>
        <Footer/>
		<Top/>
    </div>
</template>

<script>
import Header from "../components/Header.vue";
import Hero from "../components/Hero.vue";
import Products from "../components/Products.vue";
import Top from "../components/Top.vue";
import Company from "../components/Company.vue";
import Footer from "../components/Footer.vue";
import Pricing from "../components/Pricing.vue";

export default {
    name: "Home",
	components: {
        Header,
        Hero,
        Products,
        Top,
        Company,
        Footer,
        Pricing
    }
};
</script>

<style lang="scss">
.home {
	width: 100%;
	height: 100%;
}
</style>