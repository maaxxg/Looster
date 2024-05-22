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
            <span>Looster</span> is an online chat application, we try to bring people together all over the world and connect them in the simplest and most accessible way. The application can be accessed via a mobile device and a computer, but the user needs a phone number to create his own user account. We try to provide users with maximum security and keep their private things as such, and this is made possible by the high-end encryption that we used when creating Luuster itself.
        </p>
    </div>
    <div class="right">
        <img src="/about.svg" alt="">
    </div>
</div>
<br><br><br>
<hr>
<br><br><br>
<div class="team">
    <h2>Meet the Team</h2>
    <div class="members">
        <div class="mem1">
            <img src="/pfp/maks.png" alt="">
            <h3>Maks Gregorić</h3> 
            <h6>makregoric2@gmail.com</h6>
            <p>
                Main Developer,
                Team leader.
                Sigma
            </p>
        </div>
        <div class="mem2">
            <img src="/pfp/marko.png" alt="">
            <h3>Marko Eror</h3>
            <h6>darkblueshard@gmail.com</h6>
            <p>
                Web-Designer, Graphic-designer
            </p>
    
        </div>
        <div class="mem3">
            <img src="/pfp/bartolec.png" alt="">
            <h3>Lovro Bartolec</h3>
            <h6>orvol.bartolec@gmail.com</h6>
            <p>
                Assets writer, SEO specialist, Developer
            </p>
    
        </div>
        <div class="mem4">
            <img src="/pfp/vili.png" alt="">
            <h3>Vili Cenko</h3>
            <h6>cenkovili11@gmail.com</h6>
            <p>
                Tester, Developer, Presenter
            </p>
    
        </div>
        <div class="mem5">
            <img src="/pfp/vlad.png" alt="">
            <h3>Vladislav Grego</h3>
            <h6>vladislavgrego10@gmail.com</h6>
            <p>
                Tester, Marketing specialist, presenter
            </p>
    
        </div>
        <div class="mem6">
            <img src="/pfp/grso.png" alt="">
            <h3>Lovro Gršić</h3>
            <h6>lovro.grsic@gmail.com</h6>
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
        align-items: flex-end;
        margin-top: 5px;
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
        width: 90%;
        line-height: 25px;
        letter-spacing: .8px;
    }

    .right img {
        max-width: 60%;
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
        justify-content: flex-start;
        text-align: center;
        padding: 5px 0;
        border-radius: 10px;
        transition: all .4s;
    }

    .members div:hover {
        background-color: #444;
    }

    h3 {
        margin: 10px 0 0 0;
    }

    h6 {
        margin: 0;
        color: #a1a1a1;
        font-size: 12px;
    }

    hr {
        border: 2px solid #444;
        padding: 0;
        margin: 0;
    }

    .members p {
        font-size: 15px;
        color: var(--neutralLight-color);
    }

    @media only screen and (max-width: 1300px) {
        .right img {
            max-width: 80%;
        }
    }

    @media only screen and (max-width: 1150px) {
        .right img {
            max-width: 100%;
        }
    }

    @media only screen and (max-width: 1000px) {
        .right {
            display: none;
        }
        .left {
            width: 100%;
            padding: 10px;
        }

        .left p {
            text-align: justify;
            padding: none;
            width: 100%;
            margin-top: 0;
        }

        h1 {
            text-align: center;
        }

        .main {
            justify-content: center;

        }
    }

    @media only screen and (max-width: 1000px) {
        .members div {
            width: 33%;
        }

        h2 {
            text-align: center;
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