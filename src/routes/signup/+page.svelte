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
            <span>Email adress</span>
            <InputPrimary placeholder="johndoe@gmail.com" />
            <span>Password</span>
            <InputPrimary placeholder=".........." />
            <ButtonPrimary message="Signup"/>
            <br>
            <span>
                <div class="checkbox-wrapper-23">
                    Accept <a href="/" id="lol">Terms and Conditions</a>
                    <input type="checkbox" id="check-23"/>
                    <label for="check-23" style="--size: 30px">
                    <svg viewBox="0,0,50,50">
                        <path d="M5 30 L 20 45 L 45 5"></path>
                    </svg>
                    </label>
                </div>
            </span>
        </div>
    </Card>
    <br>
    <span>Already have an account? <a href="/login"><span class="accent">Login!</span></a></span>
</div>
  
<style>
    .logoContainer {
        height: 10vh;
    }
    .container{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: 90vh;
    }

    .innerCard {
        display: flex;
        flex-direction: column;
        width: 260px;
    }
    a{
        text-decoration: none;
        color: white;
        transition: all .5s;
    }
    .accent {
        color: var(--primary-color);
        font-weight: 350;}
    #lol{
        font-size: 16px;
        color: var(--primary-color);
    }

    a:hover {
        opacity: 0.7;
    }

    .checkbox-wrapper-23 *,
    .checkbox-wrapper-23 *:after,
    .checkbox-wrapper-23 *:before {
      box-sizing: border-box;
    }
    .checkbox-wrapper-23 {
        display: flex;
        justify-content: space-between;
    }
    .checkbox-wrapper-23 input {
      position: absolute;
      opacity: 0;
    }
      
    .checkbox-wrapper-23 input:checked + label svg path {
      stroke-dashoffset: 0;
    }
      
    .checkbox-wrapper-23 input:focus + label {
      transform: scale(1.03);
    }
  
    .checkbox-wrapper-23 input + label {
      display: inline-block;
      border: 2px solid var(--primary-color);
      width: 25px;
      height: 25px;
      border-radius: 6px;
      cursor: pointer;
      transition: all .2s ease;
    }
      
    .checkbox-wrapper-23 input + label:active {
      transform: scale(1.05);
      border-radius: 12px;
    }
      
    .checkbox-wrapper-23 input + label svg {
      pointer-events: none;
      padding: 5%;
    }
  
    .checkbox-wrapper-23 input + label svg path {      
      fill: none;     
      stroke: var(--primary-color);
      stroke-width: 4px;
      stroke-linecap: round;
      stroke-linejoin: round;
      stroke-dasharray: 100;
      stroke-dashoffset: 101;
      transition: all 250ms cubic-bezier(1,0,.37,.91);
    }
</style>