<script>
  import Socials from "./Socials.svelte";
</script>

<section>
  <div class="gradient-bg">
    <!-- <Socials /> -->
    <picture>
      <source
        media="(min-width: 768px)"
        srcset="images/image-profile-tablet.webp"
      />
      <source
        media="(min-width: 1200px)"
        srcset="images/image-profile-desktop.webp"
      />
      <img
        src="images/image-profile-mobile.webp"
        alt="profile"
        class="profile"
      />
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
    gap: 40px;
  }
  .gradient-bg {
    align-self: center;
    display: flex;
    flex-direction: column;
    width: 174px;
    padding-inline: 4px;
    justify-content: space-between;
    background: linear-gradient(
      180deg,
      rgba(36, 36, 36, 0) 0.65%,
      #242424 100%
    );
  }

  img.profile {
    width: 174px;
    height: 242px;
    object-fit: cover;
    object-position: 0 90%;
  }

  .intro {
    display: flex;
    flex-direction: column;
    gap: 24px;
    align-items: center;
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
      justify-content: unset;
      position: relative;
    }

    .gradient-bg {
      grid-area: gradient-bg;
      width: fit-content;
      justify-self: flex-end;
    }
    .intro {
      position: absolute;
      right: 50%;
      height: 100%;
      padding-inline: 2rem;
      grid-area: intro;
      align-items: flex-start;
      text-align: start;
      justify-content: space-between;
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

    img.profile {
      width: 349.854px;
      height: 486px;
      object-fit: cover;
      object-position: 0 90%;
    }
  }
</style>
