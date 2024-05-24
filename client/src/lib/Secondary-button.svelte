<script>
    export let message = "";
    export let inverted = false;
    export let flat = false;
</script>

<button on:click class:flat={flat} class:inverted={inverted}> {message} </button>

<style>
    button {
        outline: none;
        border: none;
        border-radius: 8px;
        padding: 12px 40px;
        font-size: 16px;
        font-weight: 500;
        color: var(--foreground-color);
        background-color: var(--secondary-color);
        cursor: pointer;
        box-shadow: 0px 2px 3px rgba(0, 0, 0, 0.9);
        margin: 5px 0;
    }

    button.inverted {
        background-color: var(--foreground-color);
        color: var(--secondary-color);
        /* border: var(--secondary-color) 2px solid; */
    }

    button:hover {
        opacity: 0.9;
    }

    button.flat {
        box-shadow: 0px 2px 3px rgba(0, 0, 0, 0.0);
    }
</style>