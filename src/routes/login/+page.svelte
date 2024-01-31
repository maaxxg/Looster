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
<LogoLong />
<div class="container">

    <Card>
        <label>Username</label>
        <InputPrimary />
        <label>Password</label>
        <InputPrimary />
        <ButtonPrimary message="Login"/>
        <a href="https://pornhub.com" id="lol">Trouble logging in?</a>
    </Card>
    <p>Dont have an account? <a href="/signup"><span class="accent">Create one!</span></a></p>
</div>
<style>
    .container{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 95vh;
    }
    a{
        text-decoration: none;
        color: white;
    }
    .accent {
        color: var(--primary-color);
        font-weight: 350;}
    #lol{
        font-size: 12px;
        color: var(--primary-color);
    }
    
</style>