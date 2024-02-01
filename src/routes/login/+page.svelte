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
</div>
<div class="container">

    <Card>
        <div class="innerCard">
            <span>Username</span>
            <InputPrimary placeholder="John Doe" />
            <span>Password</span>
            <InputPrimary placeholder="............" />
            <br>
            <ButtonPrimary type="password" message="Login"/>
            <span>
                <a href="/" id="troubleLogin">Trouble logging in?</a>
            </span>
        </div>
    </Card>
    <p>Dont have an account? <a href="/signup"><span class="accent">Create one!</span></a></p>
</div>
<style>
    .logoContainer {
        height: 10vh;
    }

    .innerCard {
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        width: 260px;
        height: 240px;
    }
    .container{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 90vh;
    }
    a{
        text-decoration: none;
        color: white;
        transition: all .5s;
    }
    .accent {
        color: var(--primary-color);
        font-weight: 350;}
    #troubleLogin{
        font-size: 16px;
        color: var(--primary-color);
    }
    
    a:hover {
        opacity: 0.7;
    }
</style>