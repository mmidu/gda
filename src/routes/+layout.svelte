<script lang="ts">
	import { onNavigate } from "$app/navigation"
    const { children } = $props()

    onNavigate((navigation) => {
        if (!document.startViewTransition) return

        return new Promise((resolve) => {
            document.startViewTransition(async () => {
                resolve()
                await navigation.complete
            })
        })
    })
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

{@render children()}