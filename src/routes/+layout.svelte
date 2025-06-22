<script lang="ts">
    import { fade } from 'svelte/transition'

    const { children, data } = $props()
</script>

<nav>
    <ul>
        <li>
            <a href="/">Home</a>
        </li>
        <li>
            <a href="/works">Works</a>
        </li>

        <li>
            <a href="/crochet">Crochet</a>
        </li>
    </ul>
</nav>

{#key data.currentRoute}
	<main in:fade={{ duration: 150, delay: 150 }} out:fade={{ duration: 150 }}>
		{@render children()}
	</main>
{/key}