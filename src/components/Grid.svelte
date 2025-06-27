<script lang="ts">
    export let data : string[]
</script>
<ul>
    {#each data as src}
        <img src={src as string} alt={'alt'}/>
    {/each}
    <li>uno</li>
    <li>due</li>
    <li>tre</li>
</ul>