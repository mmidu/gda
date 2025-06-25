<script lang="ts">
    import logo from '$lib/assets/logo.png';
    let hide = false

    function handleClick() {
        hide = true
    }

</script>


<button class={{ logo, hide }} on:click={handleClick}>
    <img src={logo} alt="Logo Giulia d'Alessandro" />
</button>

<style lang="scss">
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
    animation: fadeIn 1.5s ease-in-out;

    img {
        max-width: 300px;
        cursor: pointer;
    }
}
.hide {
    opacity: 0;
    pointer-events: none;
    transition: opacity 1.5s ease-in-out;

}


@keyframes fadeOut {
    from { opacity: 1; }
    to { opacity: 0; }
}

@keyframes hide {
    from { display: block; }
    to { display: block; }
}

@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

</style>