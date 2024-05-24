<div class="logo-long">
    <div class="inner-container">
        <h1 class="logo-heading">LOOSTER</h1>
        <p class="logo-p">The new way of <span class="logo-span">instant<br> messaging</span></p>
    </div>
</div>

<style>
    h1{
        font-size: 28px;
        color: var(--primary-color);
        margin: 0;
        padding: 0;
    }

    .logo-long {
        display: flex;
        align-items: center;
    }

    .inner-container {
        display: flex;
        align-items: center;
        transition: all .3s;
    }

    .inner-container:hover{
        opacity: 0.8;
    }

    p {
        margin-left: 12px;
        line-height: 22px;
        font-weight: 200;
        letter-spacing: .5px;
    }

    span {
        color: var(--primary-color);
        font-weight: 400;
    }
</style>