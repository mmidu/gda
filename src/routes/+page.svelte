<script lang="ts">
    import logo from '$lib/assets/logo.png';
    import { base } from '$app/paths'

</script>

<a class={['logo']} href='{base}/menu'>
    <img src={logo} alt="Logo Giulia d'Alessandro" />
</a>

<style lang="scss">

$animation-duration: 1.2s;

.logo {
    all: unset;
    margin: 0;
    padding: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    width: 100%;
    opacity: 1;
    animation: fadeIn $animation-duration ease-in-out;

    img {
        max-width: 300px;
        cursor: pointer;
    }
}

@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

</style>