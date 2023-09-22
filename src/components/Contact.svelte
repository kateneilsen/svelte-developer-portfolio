<script>
  import Socials from "./Socials.svelte";
</script>

<section>
  <div class="contact-info">
    <h1>Contact</h1>
    <p>
      I would love to hear about your project and how I could help. Please fill
      in the form, and I’ll get back to you as soon as possible.
    </p>
  </div>
  <form>
    <input type="text" id="name" placeholder="NAME" />
    <input type="text" id="name" placeholder="EMAIL" />
    <textarea id="message" placeholder="MESSAGE" />
    <button class="send">SEND MESSAGE</button>
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

  input,
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
      margin-block-start: 0;
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
