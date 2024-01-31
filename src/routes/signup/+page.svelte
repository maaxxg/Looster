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
        <label>Email adress</label>
        <InputPrimary />
        <label>Password</label>
        <InputPrimary />
        <ButtonPrimary message="Signup"/>
        <p>Accept <a href="https://www.primasolvent.hr/en/home/" id="lol">Terms and Conditions</a><input type="checkbox"/>
    </p>
        </Card>
    <p>Already have an account? <a href="/login"><span class="accent">Login!</span></a></p>
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
        font-size: 16px;
        color: var(--primary-color);
    }
    
</style>