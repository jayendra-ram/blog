<script lang="ts">
	export let description: string;
	export let slug = '';

	const href = slug && `/posts/${slug}`;
</script>

<p>
	{description}

	{#if slug}
		<a {href}>read &rarr;</a>
	{/if}
</p>

<style>
	p {
		margin: 0;
		margin-bottom: calc(var(--spacing-unit) * 8);
	}
</style>
