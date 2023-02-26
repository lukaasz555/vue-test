<template>
	<h1>{{ message }}</h1>
	<ul>
		<SingleItem
			v-for="item in storedResources"
			v-bind="item"
			:key="item.id"
		></SingleItem>
	</ul>
</template>

<script>
import SingleItem from './components/SingleItem.vue';
export default {
	data() {
		return {
			message: 'test message',
			storedResources: [
				{
					id: 0,
					title: 'First item',
					description: `Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.`,
					link: 'https://github.com/lukaasz555/vue-test',
				},

				{
					id: 1,
					title: 'Second one',
					description: `Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.`,
					link: 'https://github.com/lukaasz555/vue-test',
				},
			],
		};
	},
	components: {
		SingleItem,
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

ul {
	display: flex;
	flex-direction: column;
	align-items: center;
	width: 80%;
	margin: 1em auto;
}

h1 {
	text-align: center;
	margin: 2em 0;
}

button {
	border: none;
	background: transparent;
	cursor: pointer;
}

a {
	text-decoration: none;
	color: orange;
}
a:hover {
	text-decoration: underline;
}
</style>
