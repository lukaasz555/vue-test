<template>
	<BaseCard>
		<header>
			<h3>
				{{ title }} <span>({{ id }})</span>
			</h3>
			<base-button>remove</base-button>
		</header>
		<section>
			<p>
				{{ description }}
			</p>
			<a :href="link">Learn More</a>
		</section>
	</BaseCard>
</template>

<script>
import BaseCard from '../UI/BaseCard.vue';
export default {
	props: ['title', 'id', 'description', 'link'],
	components: { BaseCard },
};
</script>

<style scoped>
header {
	display: flex;
	justify-content: space-between;
	align-items: center;
	margin-bottom: 0.75em;
}

a {
	display: block;
	margin: 1em 0 0;
}
</style>
