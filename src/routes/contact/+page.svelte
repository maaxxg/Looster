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
    <form action="https://api.web3forms.com/submit" method="POST">        
        <Card>
            <h1>Contact us</h1>
            <input type="hidden" name="access_key" value="9d29d1e7-703e-4858-9b4f-fc42bc0e3504">
            <InputPrimary name="name" placeholder="Name"/>
            <InputPrimary name="email" placeholder="Email"/>
            <textarea name="message" placeholder="Message" cols="32" rows="10"/>
            <button type="submit">Send</button>
        </Card>
    </form>
</div>

<style>
   .logoContainer {
        height: 10vh;
    }
    a{
        text-decoration: none;
        color: white;
        transition: all .5s;
    }
    .container{
        height: 90vh;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    textarea {
        background-color: #6F6D6D;
        border: 1px solid #6147D7;
        border-radius: 5px;
        padding: 8px 15px;
        margin: 5px 0;
        color: #fff;
        outline: none;
    }
    textarea::placeholder {
        color: #aaa;
    }
    button {
        background-color: #6147D7;
        color: white;
        border: none;
        border-radius: 8px;
        outline: none;
        padding: 12px 45px;
        font-weight: 500;
        cursor: pointer;
        box-shadow: 0px 2px 2px rgb(0,0,0, 0.7);
        margin: 5px 0;
        transition: all .3s;
        font-size: 16px;
    }
    button:hover {
        opacity: 0.9;
    }
</style>