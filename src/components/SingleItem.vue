<template>
	<li>
		<header>
			<h3>
				{{ title }} <span>({{ id }})</span>
			</h3>
			<button>remove</button>
		</header>
		<section>
			<p>
				{{ description }}
			</p>
			<a :href="link">Learn More</a>
		</section>
	</li>
</template>

<script>
export default {
	props: ['title', 'id', 'description', 'link'],
};
</script>

<style scoped>
li {
	background-color: rgb(245, 245, 245);
	list-style: none;
	padding: 1.5em 2em;
	margin-bottom: 1em;
	border-radius: 12px;
	position: relative;
	z-index: 0;
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

header {
	display: flex;
	justify-content: space-between;
	align-items: center;
	margin-bottom: 0.75em;
}

header button {
	color: gray;
	border: 1px solid;
	border-radius: 6px;
	padding: 0.5em 1em;
	transition: color 0.15s, border 0.15s;
}
header button:hover {
	color: #131313;
	border: 1px solid;
}

a {
	display: block;
	margin: 1em 0 0;
}
</style>
