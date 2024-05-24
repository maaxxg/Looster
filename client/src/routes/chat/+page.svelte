<script lang="ts">
  import { idStore } from "../../services/id";
  import { sendMessage } from "../../socket";
  import { messagesStore } from "../../state/messages";
  import Card from "../../lib/Card.svelte"
  import LogoLong from "../../lib/Logo-long.svelte"
  import Message from "../../lib/Message.svelte"
  import { each } from "svelte/internal";

  let messageInput = "";
  let signedOut = true;
  let name = ""
  let displayName=""

  function signin() {
        if(name == "" ) {
            displayName = "Guest"
        } else {
            displayName = name;
        }
        signedOut = false;
    }

  function handleSubmit() {
    if ($idStore) {
      sendMessage(messageInput, $idStore);
    }

    messageInput = "";
  }

  let listRef: HTMLElement | undefined;

  $: {
    console.log("hello?");

    if (listRef) {
      listRef.scrollTo({
        behavior: "smooth",
        top: 0,
      });
    }
  }
</script>

<div class="signin logoContainer">
  <a class="signin" href="/">
      <LogoLong />
  </a>
</div>
<div class="container" class:signedOut={!signedOut}>

  <Card>
      <div class="innerCard">
          <span>Display name</span>
          <input required bind:value={name} class="signin" placeholder="username123" />
          <button type="submit" on:click={signin} class="signin">Sign up</button>
          <br>
          <!-- <span>
              <div class="checkbox-wrapper-23">
                  Accept <a id="lol">Terms and Conditions</a>
                  <input class="signin" required type="checkbox" id="check-23"/>
                  <label for="check-23" style="--size: 30px">
                  <svg viewBox="0,0,50,50">
                      <path d="M5 30 L 20 45 L 45 5"></path>
                  </svg>
                  </label>
              </div>
          </span> -->
      </div>
  </Card>
  <br>
</div>

<div class:signedOut={signedOut} id="message-container">
  <div class="list-wrapper">
    <ul bind:this={listRef}>
      {#each $messagesStore.reverse() as message}
        <li class="message-wrapper">
          {#if message.userid === $idStore}
            <div />
          {/if}

          <p class="message" class:user-message={message.userid === $idStore}>
            {message.content}
          </p>

          {#if message.userid !== $idStore}
            <div />
          {/if}
        </li>
      {/each}
    </ul>
  </div>
</div>

<form class:signedOut={signedOut} on:submit|preventDefault={handleSubmit} id="send-container">
  <input type="text" autocomplete="off" id="message-input" bind:value={messageInput} placeholder="message..."/>
  <button type="submit" id="send-button"><svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" stroke="#ffffff"><g id="SVGRepo_bgCarrier" stroke-width="1"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <path d="M10.3009 13.6949L20.102 3.89742M10.5795 14.1355L12.8019 18.5804C13.339 19.6545 13.6075 20.1916 13.9458 20.3356C14.2394 20.4606 14.575 20.4379 14.8492 20.2747C15.1651 20.0866 15.3591 19.5183 15.7472 18.3818L19.9463 6.08434C20.2845 5.09409 20.4535 4.59896 20.3378 4.27142C20.2371 3.98648 20.013 3.76234 19.7281 3.66167C19.4005 3.54595 18.9054 3.71502 17.9151 4.05315L5.61763 8.2523C4.48114 8.64037 3.91289 8.83441 3.72478 9.15032C3.56153 9.42447 3.53891 9.76007 3.66389 10.0536C3.80791 10.3919 4.34498 10.6605 5.41912 11.1975L9.86397 13.42C10.041 13.5085 10.1295 13.5527 10.2061 13.6118C10.2742 13.6643 10.3352 13.7253 10.3876 13.7933C10.4468 13.87 10.491 13.9585 10.5795 14.1355Z" stroke="#ffffff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path> </g></svg></button>
</form>

<style>

.signedOut {
  display: none !important;
}

#send-container {
  position: fixed;
  bottom: 10px;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  align-items: center;

}

#message-input {
  background-color: var(--neutralDark-color);
  outline: none;
  border: 2px solid #5A5555;
  border-radius: 10px;
  width: 40vw;
  color: white;
  padding: 10px;
  margin-right: 10px;
  transition: all .4s;
}

#send-button {
  background-color: var(--primary-color);
  border: none;
  border-radius: 50%;
  width: 38px;
  height: 38px;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
  transition: all .3s;
}

#message-input:focus {
  border: 2px solid #7A7575;
}

#send-button:hover {
  opacity: 0.8;
}

#message-container {
  width: 100%;
  height: 80vh;
  overflow-y: scroll;
  scrollbar-width: none;
  display: flex;
  flex-direction: column;
}

.logoContainer {
  height: 10vh;
}
.container{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 90vh;
  width: 100%;
}

.innerCard {
  display: flex;
  flex-direction: column;
  width: 260px;
}
a.signin{
  text-decoration: none;
  color: white;
  transition: all .5s;
  width: 260px;
}

button.signin{
  outline: none;
  border: none;
  border-radius: 8px;
  padding: 12px 45px;
  font-size: 16px;
  font-weight: 500;
  color: var(--foreground-color);
  background-color: var(--primary-color);
  cursor: pointer;
  box-shadow: 0px 2px 2px rgb(0,0,0, 0.7);
  margin: 5px 0;
  transition: all .3s;
  width: 100%;
}

input.signin {
  border: none;
  outline: none;
  background-color: #6F6D6D;
  color: var(--foreground-color);
  border: var(--primary-color) 2px solid;
  border-radius: 5px;
  padding: 8px 15px;
  margin: 5px 0;
  transition: all .3s;
  width: max-width;
}
input.signin::placeholder {
  color: #aaa;
}
input.signin:focus {
  border: 2px solid #9681f7;
}

button.signin:hover {
  opacity: 0.9;
}

a.signin:hover {
  opacity: 0.7;
}
.list-wrapper {
    overflow-y: scroll;
    width: 100%;
    display: flex;
    justify-content: center;
    scrollbar-width: none;
}

  ul {
    width: 50%;
    list-style: none;
    padding: 0;
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
  }

  .message-wrapper {
    display: flex;
    justify-content: space-between;
  }

  .message {
    padding: 0.5rem 1rem;
    max-width: 50vmin;
    width: fit-content;
    color: white;
    font-size: 1.15rem;
    border-radius: 5px;
    overflow-wrap: break-word;
    background-color: rgba(194, 194, 194, 0.6);
    margin: 0;
  }

  .user-message {
    background-color: rgba(97, 71, 215, 0.6);
  }

</style>