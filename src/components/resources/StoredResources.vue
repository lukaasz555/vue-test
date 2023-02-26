<template>
	<ul v-if="resources.length > 0">
		<SingleResource
			v-for="resource in resources"
			v-bind="resource"
			:key="resource.id"
		></SingleResource>
	</ul>
	<p v-else>brak</p>
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
	inject: ['resources'],
};
</script>

<style scoped>
ul {
	display: flex;
	flex-direction: column;
	align-items: center;
}
</style>
