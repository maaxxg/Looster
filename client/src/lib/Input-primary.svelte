<script>
    export let placeholder = '';
    export let type = "text"
    export let name
    export let autocomplete = "off";
</script>
<input type="{type}" autocomplete="{autocomplete}" placeholder="{placeholder}" name="{name}">

<style>
    input {
        border: none;
        outline: none;
        background-color: #6F6D6D;
        color: var(--foreground-color);
        border: var(--primary-color) 2px solid;
        border-radius: 5px;
        padding: 8px 15px;
        margin: 5px 0;
        transition: all .3s;
    }
    input::placeholder {
        color: #aaa;
    }
    input:focus {
        border: 2px solid #9681f7;
    }
</style>
