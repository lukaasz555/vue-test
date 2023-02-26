<template>
	<li>
		<slot></slot>
	</li>
</template>

<style scoped>
li {
	background-color: rgb(245, 245, 245);
	list-style: none;
	padding: 1.5em 2em;
	border-radius: 12px;
	position: relative;
	z-index: 0;
	width: 80%;
	margin: 1em auto;
}

li::before {
	content: '';
	position: absolute;
	border-radius: 12px;
	left: 0;
	width: 100%;
	top: 0;
	height: 100%;
	box-shadow: 4px 8px 22px rgba(0, 0, 0, 0.05);
	transition: box-shadow 0.25s;
	z-index: -10;
}

li:hover::before {
	box-shadow: 4px 8px 22px rgba(0, 0, 0, 0.15);
}
</style>
