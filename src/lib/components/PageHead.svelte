<script lang="ts">
	export let title: string;
	export let description: string;

	const siteTitle = 'jay\'s blog';
	const formattedTitle = title ? `${title} | ${siteTitle}` : siteTitle;
</script>

<svelte:head>
	<title>{formattedTitle}</title>
	<meta property="og:site_name" content={siteTitle} />
	<meta property="og:title" content={title} />
	<meta property="og:description" content={description} />
</svelte:head>

<!-- make color blue -->
<style>
	:header {
		background-color: blue;
	}

</style>