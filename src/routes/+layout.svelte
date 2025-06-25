<script lang="ts">
    import { fade } from 'svelte/transition'
    import { base } from '$app/paths'
    const { children, data } = $props()
</script>

<!--
<nav>
    <ul>
        <li>
            <a href="{base}/">Home</a>
        </li>
        <li>
            <a href="{base}/works">Works</a>
        </li>

        <li>
            <a href="{base}/crochet">Crochet</a>
        </li>
    </ul>
</nav>
-->

{#key data.currentRoute}
	<main in:fade={{ duration: 150, delay: 150 }} out:fade={{ duration: 150 }}>
		{@render children()}
	</main>
{/key}