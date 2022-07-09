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
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";
import Products from "./components/Products.vue";
import Top from "./components/Top.vue";
import Company from "./components/Company.vue";
import Footer from "./components/Footer.vue";
import Pricing from "./components/Pricing.vue";

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
* {
    padding: 0;
    margin: 0;

	font-family: "visby";
}

html,
body {
	width: 100%;
	height: 100%;

	scroll-behavior: smooth;
	background-color: rgb(250, 250, 250);
	//overflow-x: hidden;
}

.home {
	width: 100%;
	height: 100%;
}

/* width */
::-webkit-scrollbar {
  width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
  background: white;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: var(--color-green);
  border-radius: 10px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: var(--color-yellowGreen);
}

@font-face {
	font-family: "visby";
	src: url("./assets/fonts/VisbyCF-ExtraBold.woff2");
	font-weight: 800;
	font-style: normal;
}

@font-face {
	font-family: "visby";
	src: url("./assets/fonts/VisbyCF-DemiBold.woff2");
	font-weight: 600;
	font-style: normal;
}

@font-face {
	font-family: "visby";
	src: url("./assets/fonts/VisbyCF-Regular.woff2");
	font-weight: 400;
	font-style: normal;
}


:root {
	--color-green: #5dd39e;
	--color-blue: #1c37a3;
	--color-blue-light: #425ab9;
	--color-yellowGreen: #bce784;
	--logo-sideSpacing: 5rem;
	--footer-padding: 3rem;
	--color-blue-filter: invert(15%) sepia(80%) saturate(2365%) hue-rotate(222deg) brightness(104%) contrast(102%);
}
</style>
