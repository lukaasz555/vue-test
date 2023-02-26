<template>
	<button :class="mode">
		<slot></slot>
	</button>
</template>

<script>
export default {
	props: ['mode'],
};
</script>

<style scoped>
button {
	padding: 0.5rem 1.25rem;
	font-family: inherit;
	background-color: #2c666e;
	border: 1px solid #2c666e;
	color: white;
	cursor: pointer;
	border-radius: 6px;
}

button:hover,
button:active {
	background-color: #07393c;
	border-color: #07393c;
}

.flat {
	background-color: transparent;
	color: #07393c;
	border: none;
}

.flat:hover,
.flat:active {
	color: white;
	background-color: #2c666e;
}
</style>
