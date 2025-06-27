<script lang="ts">
    import { fade } from 'svelte/transition'
    const { children, data } = $props()
</script>


{#key data.currentRoute}
	<main in:fade={{ duration: 150, delay: 150 }} out:fade={{ duration: 150 }}>
		{@render children()}
	</main>
{/key}