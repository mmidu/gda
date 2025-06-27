<script lang="ts">
    import { base } from '$app/paths'
</script>

<ul class={['menu']}>
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
    text-align: center;
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


</style>