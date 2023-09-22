<script>
  import Socials from "./Socials.svelte";
  import Input from "./Input.svelte";

  let isValidEmail;
  let isValidName;
  let email;
  let name;

  const validateForm = () => {
    console.log(email);
    isValidEmail = email
      .toLowerCase()
      .match(
        /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|.(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
      );
    isValidName = name.length >= 1;
  };
</script>

<section>
  <div class="contact-info">
    <h1>Contact</h1>
    <p>
      I would love to hear about your project and how I could help. Please fill
      in the form, and I’ll get back to you as soon as possible.
    </p>
  </div>
  <form novalidate on:submit|preventDefault={validateForm}>
    <Input
      type="text"
      le
      id="name"
      placeholder="Name"
      bind:value={name}
      isValid={isValidName}
      error="Sorry, your name is required."
    />
    <Input
      type="email"
      id="email"
      placeholder="Email"
      isValid={isValidEmail}
      error="Sorry, invalid format here."
      bind:value={email}
    />
    <textarea id="message" placeholder="MESSAGE" />
    <button type="submit" class="send">SEND MESSAGE</button>
  </form>
  <hr />
  <h4>adamkeyes</h4>
  <span class="socials">
    <Socials />
  </span>
</section>

<style>
  section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    padding-block-start: 60px;
    background-color: var(--darkgrey);
    background-repeat: repeat-x;
    align-items: center;
    width: 100% !important;
  }

  .contact-info {
    width: 345px;
  }

  form {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    gap: 2rem;
    margin-block-start: 50px;
    width: 345px;
  }
  textarea {
    border: none;
    border-bottom: 1px solid var(--white);
    background: none;
    color: var(--white);
    padding-block-end: 1rem;
    padding-inline-start: 24px;
    text-transform: uppercase;
  }

  textarea {
    resize: none;
    height: 107px;
  }

  textarea:focus {
    outline: none;
    border-bottom: 1px solid var(--green);
  }

  button.send {
    align-self: end;
  }

  hr {
    margin-block-start: 87px;
  }
  hr:last-of-type {
    margin-block-end: 20px;
  }

  @media (min-width: 768px) {
    section {
      align-items: center;
      padding-inline: 2rem;
    }
    .contact-info {
      width: 445px;
    }
    form {
      width: 445px;
    }
  }

  @media (min-width: 1200px) {
    section {
      width: 100%;
      display: grid;
      grid-template-columns: 1fr 1fr;
      text-align: start;
      padding-inline: 0;
    }

    .contact-info {
      width: 445px;
      align-self: flex-start;
      display: flex;
      flex-direction: column;
      gap: 36px;
    }
    form {
      width: 445px;
      align-self: flex-start;
    }
    hr {
      grid-column: 1/3;
    }
    h4 {
      grid-column: 1/2;
    }
    span.socials {
      grid-column: 2/3;
      justify-self: flex-end;
    }
  }
</style>
