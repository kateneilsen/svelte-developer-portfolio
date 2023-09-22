<script>
  import Socials from "./Socials.svelte";
</script>

<section>
  <h4 class="mobile">adamkeyes</h4>
  <div class="gradient-bg">
    <Socials />
    <picture>
      <source
        media="(min-width: 768px)"
        srcset="images/image-profile-tablet.webp"
      />
      <source
        media="(min-width: 1200px)"
        srcset="images/image-profile-desktop.webp"
      />
      <img src="images/image-profile-mobile.webp" alt="profile" />
    </picture>
  </div>

  <div class="intro">
    <h1>
      Nice to <br /> meet you! <br />
      I'm <br /> <span class="underline">Adam Keyes</span>.
    </h1>
    <p>
      Based in the UK, I’m a front-end developer passionate about building
      accessible web apps that users love.
    </p>
    <button>CONTACT ME</button>
  </div>
</section>

<style>
  section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    align-items: center;
    z-index: 2;
  }

  .gradient-bg {
    display: flex;
    flex-direction: column;
    gap: 20px;
    background-image: linear-gradient(
      180deg,
      rgba(36, 36, 36, 0) 0.65%,
      #242424 100%
    );
  }

  img {
    width: 174px;
    height: 242px;
    object-fit: cover;
    object-position: 0 90%;
  }

  .intro {
    padding-block-start: 40px;
    display: flex;
    flex-direction: column;
    gap: 24px;
    align-items: center;
    width: 345px;
  }

  .underline {
    text-decoration: underline;
    text-decoration-style: 2px solid;
    text-decoration-color: var(--green);
  }
  br:first-of-type {
    display: none;
  }
  br:last-of-type {
    display: none;
  }

  @media (min-width: 768px) {
    section {
      display: grid;
      width: 100%;
      justify-content: flex-end;
      position: relative;
    }

    h4 {
      position: absolute;
      top: 20px;
      left: 2rem;
    }

    .gradient-bg {
      width: fit-content;
      justify-self: flex-end;
      align-items: flex-end;
      background-image: linear-gradient(
        1deg,
        rgba(36, 36, 36, 0) 0.65%,
        #242424 100%
      );
      background-origin: border-box;
    }
    .intro {
      height: 100%;
      padding-inline: 2rem;
      padding-block-start: 0;
      align-items: flex-start;
      text-align: start;
      position: absolute;
      gap: 2rem;
      top: 140px;
    }

    h1 {
      width: 445px;
      letter-spacing: -2.045px;
    }
    p {
      width: 445px;
    }

    br:first-of-type {
      display: block;
    }
    br:not(:last-of-type, :first-of-type) {
      display: none;
    }

    br:last-of-type {
      display: block;
    }

    img {
      width: 322px;
      height: 500px;
      object-fit: cover;
    }
  }

  @media (min-width: 1200px) {
    section {
      padding-inline-start: 2rem;
      padding-inline-end: 0;
    }
    img {
      width: 445px;
      height: 618px;
      object-fit: cover;
      object-position: 0 80%;
    }

    .intro {
      justify-content: flex-start;
      gap: 3rem;
      width: unset;
    }

    h1 {
      width: 100%;
    }

    br:first-of-type {
      display: none;
    }

    br:last-of-type {
      display: none;
    }
  }
</style>
