<script>
  import Socials from "./Socials.svelte";
</script>

<section>
  <h1>Contact</h1>
  <p>
    I would love to hear about your project and how I could help. Please fill in
    the form, and I’ll get back to you as soon as possible.
  </p>
  <form>
    <input type="text" id="name" placeholder="NAME" />
    <input type="text" id="name" placeholder="EMAIL" />
    <textarea id="message" placeholder="MESSAGE" />
    <button class="send">SEND MESSAGE</button>
  </form>
  <hr />
  <Socials />
</section>

<style>
  section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    padding-block-start: 60px;
    background-color: var(--darkgrey);
    width: 100%;
  }

  form {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    gap: 2rem;
    margin-block-start: 50px;
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
    h1,
    p,
    form {
      width: 445px;
    }
  }
</style>
