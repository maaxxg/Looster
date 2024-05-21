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
    import { createDropdownMenu, melt } from '@melt-ui/svelte'
    
    
    let show = false;
    const {
        elements: { menu, item, trigger, arrow }
    } = createDropdownMenu()
</script>

<nav>
    <div id="logo-desktop">
        <LogoLong />
    </div>
    <div id="logo-mobile">
        <LogoShort />
    </div>
    <ul class="nav-links">
        <Link>About us</Link>
        <Link href="contact">Contact us</Link>
        <a href="/login">
            <ButtonPrimary width="30px" class="loginBtn" inverted = "true" message="Log in" />
        </a>
    </ul>
    <button class="nav-menu-btn" use:melt={$trigger}><img src="/menu.svg" alt=""></button>
    <div class="nav-menu" use:melt={$menu}>
        <div class="mobile-nav-link" use:melt={$item}><Link>About us</Link></div>
        <div class="mobile-nav-link" use:melt={$item}><Link>Contact us</Link></div>
        <div class="mobile-nav-link mobile-login" use:melt={$item}>
            <a href="/login">
                <ButtonPrimary width="30px" class="loginBtn" inverted = "true" message="Log in" />
            </a>
    </div>
    <div use:melt={$arrow} />
    </div>
</nav>

<main>
    <div class="left">
        <h1>We'll help <br> 
        <div class="type-container">
            <div class="typed">Connect</div>
            </div>
        </h1>
        <a href="/signup">
            <ButtonPrimary id="createAccount" message="Create Account" />
        </a>
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
        max-width:1000px;
    }

    h1 {
        font-size: 5rem;
        font-weight: 400;
        margin: 10vh 0;
    }
    a{
        text-decoration: none;
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

    .nav-menu-btn {
        border: none;
        outline: none;
        background-color: var(--background-color);
        color: white;
        transition: all .3s;
        display: none;
    }

    .nav-menu {
        display: none;
        background-color: var(--primary-color);
        padding: 20px 10px;
        border-radius: 5px;

    }

    #logo-mobile {
        display: none;
        margin: 10px 0;
    }

    @media only screen and (max-width: 1200px) {
        .right {
            display: none;
        }
        main {
            width: 100%;
            align-items: center;
        }
    }
    @media only screen and (max-width: 800px) {
        .left {
            width: 100%;
            text-align: center;
        }
        .left h1{
            font-size: 4rem;
        }

        .typed {
            font-size: 4.5rem;
        }

        .nav-links {
            display: none;
        }

        .nav-menu-btn {
            display: block;
        }

        .nav-menu {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            height: fit-content;
        }

        .mobile-nav-link {
            margin: 8px 0;
        }

    }

    @media only screen and (max-width: 400px) {
        .left h1 {
            font-size: 3rem;
        }
        .typed {
            font-size: 3.5rem;
        }
        #logo-desktop {
            display: none;
        }
        #logo-mobile {
            display: block;
        }
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