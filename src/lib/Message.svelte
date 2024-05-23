<script>
    export let message;
    export let incoming=false;
    export let name="guest";
</script>
<div class="message-container">
    <div class="inner-container {incoming}">
        <h5 class="{incoming}">{name}</h5>
        <div class="message {incoming}">
            <slot>{message}</slot>
        </div>
    </div>
</div>

<style>
    .message {
        background-color: rgba(97, 71, 215, 0.6);
        width: fit-content;
        padding: 10px 10px;
        border-radius: 5px;
        font-size: 18px;
        max-width: 40vw;
    }

    .message.incoming {
        background-color: rgba(194, 194, 194, 0.6);
    }

    .message-container {
        width: 100%;
        height: fit-content;
        margin: 10px 0px;
    }
    h5 {
        margin: 3px;
        padding: 0;
        color: var(--neutralLight-color);
    }

    .inner-container {
        width: fit-content;
        display: flex;
        flex-direction: column;
    }
    .sent {
        float: right;
        align-self: flex-end;
    }
</style>