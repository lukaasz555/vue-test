<template>
	<ul>
		<SingleResource
			v-for="resource in resources"
			v-bind="resource"
			:key="resource.id"
		></SingleResource>
	</ul>
</template>

<script>
import SingleResource from './SingleResource.vue';
export default {
	data() {
		return {};
	},
	components: {
		SingleResource,
	},
	props: ['resources'],
};
</script>

<style scoped>
ul {
	display: flex;
	flex-direction: column;
	align-items: center;
	width: 80%;
	margin: 1em auto;
}
</style>
