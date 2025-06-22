<h1>Home</h1>

<div class="logo">
    LOGO
</div>


<style lang="scss">
    .logo {
        color: white;
        background-color: black;
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        position: absolute;
        z-index: 100;
        animation-name: fade-out;
        animation-timing-function: ease-out;
        animation-delay: 1s;
        animation-duration: 0.5s;
        animation-fill-mode: both;
    }

    @keyframes fade-out {
        0% {
            pointer-events: all;
            opacity: 1;
        }
        100% {
            pointer-events: none;
            opacity: 0;
        }
    }
</style>