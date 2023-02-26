<template>
	<BaseCard>
		<form @submit.prevent="handleSubmit">
			<div>
				<label for="title">Title</label
				><input type="text" id="title" name="title" ref="titleInput" />
			</div>
			<div>
				<label for="link">Link</label
				><input type="url" id="link" ref="linkInput" />
			</div>
			<div>
				<label for="desc"></label>
				<textarea
					name="description"
					id="description"
					cols="30"
					rows="3"
					ref="descTextarea"
				></textarea>
			</div>

			<div>
				<base-button type="submit">Add Resource</base-button>
			</div>
		</form>
	</BaseCard>
</template>

<script>
import BaseCard from '../UI/BaseCard.vue';
export default {
	data() {
		return {
			enteredTitle: '',
			enteredLink: '',
			enteredDescription: '',
		};
	},
	inject: ['addNewResource'],
	components: {
		BaseCard,
	},
	methods: {
		handleSubmit() {
			const enteredTitle = this.$refs.titleInput.value;
			const enteredLink = this.$refs.linkInput.value;
			const enteredDescription = this.$refs.descTextarea.value;
			this.addNewResource(enteredTitle, enteredDescription, enteredLink);
		},
	},
};
</script>

<style scoped>
label {
	font-weight: bold;
	display: block;
	margin-bottom: 0.5rem;
}

input,
textarea {
	display: block;
	width: 100%;
	font: inherit;
	padding: 0.15rem;
	border: 1px solid #ccc;
}

input:focus,
textarea:focus {
	outline: none;
	border-color: #07393c;
	background-color: #0b888f18;
}
textarea {
	resize: vertical;
	padding: 0.5em 0.75em;
}
.form-control {
	margin: 1rem 0;
}
</style>
