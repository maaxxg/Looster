<script>
    import Card from "$lib/Card.svelte"
    import InputPrimary from "$lib/Input-primary.svelte"
    import InputSecondary from "$lib/Input-secondary.svelte"
    import Link from "$lib/Link.svelte"
    import LogoLong from "$lib/Logo-long.svelte"
    import LogoShort from "$lib/Logo-short.svelte"
    import Modal from "$lib/Modal.svelte"
    import ButtonPrimary from "$lib/Primary-button.svelte"
    import ButtonSecondary from "$lib/Secondary-button.svelte"
    
</script>

<div class="logoContainer">
    <a href="/">
        <LogoLong />
    </a>
    <main>
        <div class="left">
            <div>
                Thank you for joining us! 
                <br><br>
                A confirmation email has been sent to the provided email address.
            </div>
            <div class="buttonContainer">
                <ButtonPrimary flat="true" message="Go to login" />
            </div>
        </div>
        <div class="right">
            <img src="/mail.svg" alt="">
        </div>
    </main>
</div>

<style>
    a {
        text-decoration: none;
        color: inherit;
    }

    .logoContainer {
        height: 10vh;
    }

    main {
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        height: 80vh;
    }

    .left {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        font-size: 1.5rem;
        width: 30vw;
    }

    .left div {
        margin: 20px 0;
    }

    .buttonContainer {
        width: 30vw;
    }

    img {
        width: 30rem;
    }

    @media only screen and (max-width: 1100px) {
        .right {
            display: none;
        }
        .left {
            width: 70vw;
        }
        .buttonContainer {
            width: 70vw;
        }
    }
</style>