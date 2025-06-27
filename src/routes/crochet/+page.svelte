<script>
	import Grid from "../../components/Grid.svelte"

    const crochetImages = Object.keys(import.meta.glob(['$lib/assets/crochet/**.jpeg'], { eager: true, query: '?url' }));

</script>
<header class={['header']}>
    <h1>Crochet</h1>
</header>
<section>
    <Grid data={crochetImages}/>
</section>

<style lang="scss">
    .header {
        border-bottom: 1px solid #7a6e66;
        text-align: end;
        padding: 1rem 2rem;

        h1 {
            margin: 0;
        }
    }
</style>