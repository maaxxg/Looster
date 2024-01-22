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
        <span class="typewriter">Connect</span>
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

    .typewriter {
        overflow: hidden; /* Ensures the content is not revealed until the animation */
        border-right: .15em solid white; /* The typwriter cursor */
        white-space: nowrap; /* Keeps the content on a single line */
        margin: 0 auto; /* Gives that scrolling effect as the typing happens */
        letter-spacing: .1em; /* Adjust as needed */
        width: 0;
        color: var(--primary-color);
        font-weight: 600;
        animation: 
            typing 3.5s step-end infinite,
            blink-caret .75s step-end infinite;
    }

    @keyframes typing {
        from { width: 0 }
        to { width: 100% }
    }

    /* The typewriter cursor effect */
    @keyframes blink-caret {
        from, to { border-color: transparent }
        50% { border-color: white; }
    }
</style>