<script lang="ts">
    import logo from '$lib/assets/logo.png';
</script>

<div class="logo">
    <img src={logo} alt="Logo Giulia d'Alessandro" />
</div>

<style lang="scss">
.logo {
    margin: 0;
    padding: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    img {
        max-width: 300px;
        cursor: pointer;
        animation: fadeIn 1.5s ease-in-out;
    }
}
@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

</style>