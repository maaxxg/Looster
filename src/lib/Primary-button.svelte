<script>
    export let message;
    export let inverted=false;
    export let flat=false;
</script>

<button class:flat={flat} class:inverted={inverted} >{message}</button>

<style>
    button{
        outline: none;
        border: none;
        border-radius: 5px;
        padding: 12px 75px;
        font-size: 16px;
        font-weight: 500;
        color: var(--foreground-color);
        background-color: var(--primary-color);
        cursor: pointer;
        box-shadow: 0px 4px 2px rgb(0,0,0);
        
    }
    button.inverted {
        background-color: var(--foreground-color);
        color: var(--primary-color);
        border: var(--primary-color) 2px solid;
    }
    button:hover {
        opacity: 0.9;
    }
    button.flat{
        box-shadow: 0px 0px 0px;
    }
</style>