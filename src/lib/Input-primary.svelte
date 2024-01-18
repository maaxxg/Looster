<script>
    export let placeholder = '';
    export let type = "text"
</script>
<input type="{type}" placeholder="{placeholder}">

<style>
    input {
        border: none;
        outline: none;
        background-color: #6F6D6D;
        color: var(--foreground-color);
        border: var(--primary-color) 1px solid;
        border-radius: 5px;
        padding: 8px 15px;
        margin: 5px 0;
    }
    input::placeholder {
        color: #aaa;
    }
</style>
