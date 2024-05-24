<script>
    export let href = "/"
</script>
<a on:click href="{href}">
    <slot></slot>
</a>

<style>
    a {
        text-decoration: none;
        color: var(--foreground-color);
        font-weight: 200;
        letter-spacing: .7px;
        font-size: 18px;
        transition: .3s;
        margin: 0 10px;
    }

    a:hover {
        opacity: 0.8;
    }
</style>