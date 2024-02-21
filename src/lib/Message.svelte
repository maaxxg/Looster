<script>
    export let message;
    export let incoming;
</script>

<div class="message" class:incoming={incoming}>
    {message}
</div>

<style>
    .message {
        background-color: rgba(97, 71, 215, 0.6);
        width: fit-content;
        padding: 10px 10px;
        border-radius: 5px;
        font-size: 18px;
        margin: 10px 5px;
        max-width: 40vw;
    }

    .incoming {
        background-color: rgba(194, 194, 194, 0.6);
    }
</style>