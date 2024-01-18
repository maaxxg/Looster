<script>
    export let showModal = false;
</script>
<div class:show={showModal} class="backdrop">
    <div class="modal">
        <slot></slot>
    </div>
</div>
<style>
    .backdrop {
        width: 100vw;
        height: 100vh;
        position: absolute;
        top: 0;
        left: 0;
        background-color: rgba(0, 0, 0, 0.7);
        z-index: 1;
        visibility: hidden;
    }

    .modal {
        z-index: 2;
        position: absolute;
        background-color: var(--neutralDark-color);
        left: 50%;
        top: 50%;
        transform: translate(-50%, -50%);
        width: fit-content;
        height: fit-content;
        display: flex;
        flex-direction: column;
        padding: 40px 100px;
        border-radius: 10px;
    }
    .show {
        visibility: visible;
    }
</style>