<template>
	<BaseCard>
		<div>
			<base-button
				@click="setSelectedOption('stored-resources')"
				:mode="handleResButtonMode"
				>Stored Resources</base-button
			>
			<base-button
				@click="setSelectedOption('add-resource')"
				:mode="handleAddButtonMode"
				>Add Resource</base-button
			>
		</div>
	</BaseCard>
	<component :is="selectedOption"> </component>
</template>

<script>
import BaseCard from '../UI/BaseCard.vue';
import AddResource from './AddResource.vue';
import StoredResources from './StoredResources.vue';

export default {
	data() {
		return {
			selectedOption: 'stored-resources',
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
	components: { BaseCard, AddResource, StoredResources },
	methods: {
		setSelectedOption(opt) {
			this.selectedOption = opt;
		},
	},
	provide() {
		return {
			resources: this.storedResources,
		};
	},
	computed: {
		handleResButtonMode() {
			return this.selectedOption === 'stored-resources' && 'flat';
		},
		handleAddButtonMode() {
			return this.selectedOption === 'add-resource' && 'flat';
		},
	},
};
</script>

<style scoped>
div > button:first-child {
	margin-right: 1em;
}
</style>
