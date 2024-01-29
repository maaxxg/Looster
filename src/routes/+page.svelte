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
    let show = false;
</script>

<nav>
    <LogoLong />
    <ul class="nav-links">
        <Link>About us</Link>
        <Link>Contact us</Link>
        <ButtonPrimary width="30px" class="loginBtn" inverted = "true" message="Log in" />
    </ul>
</nav>

<main>
    <div class="left">
        <h1>We'll help <br> 
        <div class="type-container">
            <div class="typed">Connect</div>
            </div>
        </h1>
        <ButtonPrimary id="createAccount" message="Create Account" />
    </div>
    <div class="right">
        <img src="/landingSVG.svg" alt="">
        <p>
            <span class="accent">Speed</span>, 
            <span class="accent">efficiency</span>, 
            security all in one place. 
            <span class="accent">Sign up</span> today!
        </p>
    </div>
</main>

<style>
    nav {
        display: flex;
        justify-content: space-between;
        height: 10%;
    }

    main {
        width: 100%;
        display: flex;
        justify-content: space-between;
        height: 75vh;
        align-items: center;
    }

    .left {
        width: 50%;
        display: block;
        margin: auto;
    }

    .right {
        width: 35%;
        margin: 0;
    }

    h1 {
        font-size: 5rem;
        font-weight: 400;
        margin: 10vh 0;
    }

    img {
        width: 65%;
        margin: none;
    }

    p {
        margin-top: 20px;
        font-size: 20px;
        max-width: 70%;
        font-weight: 300;
    }

    .accent {
        color: var(--primary-color);
        font-weight: 350;
    }
    .type-container{
        display: inline-block;
        font-family: monospace;
        color: var(--primary-color);
        font-size: 1.4em;
    }

    .typed {
        overflow: hidden;
        white-space: nowrap;
        width: 0;
        animation: typing 1s steps(20, end), blink 0.4s step-end infinite alternate;
        animation-fill-mode: forwards;
        border-right: 4px solid var(--primary-color);
    }

    @keyframes typing {
        from { width: 0 }
        to { width: 100% }
    }

    @keyframes blink {
        50% {
            border-color: transparent;
        }
    }
</style>