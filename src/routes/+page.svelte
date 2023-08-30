<script lang="ts">
    import type { PageData } from './$types';

    import PageHead from '$lib/components/PageHead.svelte';
    import Article from '$lib/components/Article.svelte';
    import ArticleTitle from '$lib/components/ArticleTitle.svelte';
    import ArticleMeta from '$lib/components/ArticleMeta.svelte';
    import ArticleDescription from '$lib/components/ArticleDescription.svelte';

    export let data: PageData;
</script>

<div class="header">
    <PageHead title="Home" description="jay's blog" />
</div>

{#each data.posts as { slug, title, author, description, date }}
    <Article>
        <ArticleTitle {slug} {title} />
        <ArticleMeta {author} {date} />
        <ArticleDescription {description} {slug} />
    </Article>
{/each}

<slot />

<style>
     :global(:root) {
        --spacing-unit: 4px;
        --color-background: #ffffff;
        --color-text-primary: #212121;
        --color-text-secondary: #5a5a5a;
    }

 

    .header {
        position: relative;
        z-index: 1;
        padding-left: calc(var(--spacing-unit) * 8);
        padding-right: calc(var(--spacing-unit) * 8);
        background-color: var(--color-background);
        color: var(--color-text-primary);
    }

    :global(a, a:visited, a:active) {
        text-decoration: none;
        color: var(--color-text-primary);
        font-weight: 700;
    }
</style>