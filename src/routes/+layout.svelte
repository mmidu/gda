<script lang="ts">
	import { cubicInOut, quadInOut } from 'svelte/easing';
    import { fade } from 'svelte/transition'
    const { children, data } = $props()
</script>


{#key data.currentRoute}
	<main in:fade={{ duration: 200, delay: 200, easing: cubicInOut }} out:fade={{ duration: 200, easing: cubicInOut}}>
		{@render children()}
	</main>
{/key}