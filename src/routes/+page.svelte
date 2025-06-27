<script lang="ts">
    import { base } from '$app/paths'
    import logo from '$lib/assets/logo.png';
    let hide = false

    function handleClick() {
        hide = true
    }

</script>

<ul class={['menu', {hide: !hide}]}>
    <li class={['category']}>
        <a  href="{base}/architettura">Architettura e Ristrutturazione</a>
    </li>
    <li class={['category', 'crochet']}>
        <a  href="{base}/crochet">Crochet</a>
    </li>
    <li class={['category']}>
        <a  href="{base}/consulenza">Consulenza</a>
    </li>
    <li class={['category']}>
        <a  href="{base}/contatti">Contatti</a>
    </li>
</ul>

<button class={['logo', { hide }]} on:click={handleClick}>
    <img src={logo} alt="Logo Giulia d'Alessandro" />
</button>

<style lang="scss">

$animation-duration: 1.2s;

.menu {
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 1.5em;
    align-items: center;
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    padding: 0;
    margin: 0;
    transition: opacity $animation-duration $animation-duration ease-in-out;
}
.category {
    all: unset;
    font-family: 'Helvetica Neue', sans-serif;
    font-size: 1.8rem;
    cursor: pointer;
    display: inline-block;
    font-weight: normal;
    position: relative;
    a {
        all: unset;

    }
    &::after {
        content: "";
        position: absolute;
        width: 0;
        height: 1px;
        left: 0;
        bottom: -5px;
        background-color: #7a6e66;
        transition: width 0.3s;
    }
    &:hover {
        color: #5f554f;

        &::after {
            width: 100%;
        }
    }
}
.crochet {
    font-family: 'Sacramento', cursive;
    font-size: 2.2rem;
}

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
.hide {
    opacity: 0;
    pointer-events: none;
    transition: opacity $animation-duration ease-in-out;
}

@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

</style>