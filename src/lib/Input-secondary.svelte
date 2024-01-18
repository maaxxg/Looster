<script>
    export let placeholder = '';
    export let type = "text"
</script>
<input type="{type}" placeholder="{placeholder}">

<style>
    input {
        border: none;
        outline: none;
        background-color: #2F2F2F;
        color: var(--foreground-color);
        border-radius: 5px;
        padding: 4px 18px;
    }
    input::placeholder {
        color: #888;
    }
</style>
