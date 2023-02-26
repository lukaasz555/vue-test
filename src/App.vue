<template>
	<TheHeader />
	<TheResources />
</template>

<script>
import TheHeader from './components/layouts/TheHeader.vue';
import TheResources from './components/resources/TheResources.vue';

export default {
	components: {
		TheHeader,
		TheResources,
	},
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;300;400;500;700&display=swap');

body {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
	font-family: 'Roboto', sans-serif;
}

*,
*::before,
*::after {
	margin: 0;
	padding: 0;
	box-sizing: inherit;
}

a {
	text-decoration: none;
	color: orange;
}
a:hover {
	text-decoration: underline;
}
</style>
