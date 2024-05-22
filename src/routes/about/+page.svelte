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

<div class="main">
    <div class="left">
        <h1>
            About us
        </h1>
        <br>
        <p>
            <span>Luuster</span> is an online chat application, we try to bring people together all over the world and connect them in the simplest and most accessible way. The application can be accessed via a mobile device and a computer, but the user needs a phone number to create his own user account. We try to provide users with maximum security and keep their private things as such, and this is made possible by the high-end encryption that we used when creating Luuster itself.
        </p>
    </div>
    <div class="right">
        <img src="/aboutus.svg" alt="">
    </div>
</div>
<br><br><br>
<div class="team">
    <h2>Meet the Team</h2>
    <div class="members">
        <div class="mem1">
            <img src="/pfp/maks.png" alt="">
            <h3>Maks Gregorić</h3> 
            <p>
                Main Developer,
                Team leader
            </p>
        </div>
        <div class="mem2">
            <img src="/pfp/marko.png" alt="">
            <h3>Marko Eror</h3>
            <p>
                Web-Designer, Graphic-designer
            </p>
    
        </div>
        <div class="mem3">
            <img src="/pfp/bartolec.png" alt="">
            <h3>Lovro Bartolec</h3>
            <p>
                Assets writer, SEO specialist, developer
            </p>
    
        </div>
        <div class="mem4">
            <img src="/pfp/vili.png" alt="">
            <h3>Vili Cenko</h3>
            <p>
                Tester, Developer, Presenter
            </p>
    
        </div>
        <div class="mem5">
            <img src="/pfp/vlad.png" alt="">
            <h3>Vladislav Grego</h3>
            <p>
                Tester, Marketing specialist, presenter
            </p>
    
        </div>
        <div class="mem6">
            <img src="/pfp/grso.png" alt="">
            <h3>Lovro Gršić</h3>
            <p>
                SEO specialist
            </p>
    
        </div>
    </div>
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
    .main {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    span {
        color: var(--primary-color);
        font-weight: 600;
    }

    .left, .right {
        width: 40%;
    }

    p {
        font-size: 18px;
    }

    .right img {
        max-width: 50%;
    }

    .members {
        display: flex;
        justify-content: space-evenly;
        flex-wrap: wrap;
    }

    .team img{
        width: 100px;
        border-radius: 50%;
    }

    .members div {
        display: flex;
        flex-direction: column;
        width: 16.6%;
        align-items: center;
    }

    h3 {
        margin: 10px 0 0 0;
    }

    .members p {
        font-size: 15px;
        color: var(--neutralLight-color);
    }

    @media only screen and (max-width: 850px) {
        .members div {
            width: 33%;
        }
    }

    @media only screen and (max-width: 720px) {
        .members div {
            width: 50%;
        }
    }

    @media only screen and (max-width: 550px) {
        .members div {
            width: 100%;
        }
    }

</style>