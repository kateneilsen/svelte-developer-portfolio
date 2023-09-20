<header>
  <h4>adamkeyes</h4>
  <div class="socials">
    <a href="/">
      <img src="images/icon-github.svg" alt="github" />
    </a>
    <a href="/">
      <img src="images/icon-frontend-mentor.svg" alt="frontend mentor" />
    </a>
    <a href="/">
      <img src="images/icon-linkedin.svg" alt="linkedin" />
    </a>
    <a href="/">
      <img src="images/icon-twitter.svg" alt="twitter" />
    </a>
  </div>
</header>
<section>
  <picture>
    <source
      media="(min-width: 600px)"
      srcset="images/image-profile-tablet.webp"
    />
    <source
      media="(min-width: 1200px)"
      srcset="images/image-profile-desktop.webp"
    />
    <img src="images/image-profile-mobile.webp" alt="profile" class="profile" />
  </picture>
  <div class="intro">
    <h1>
      Nice to meet you! <br />
      I'm <span class="underline">Adam Keyes</span>.
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
    text-align: center;
  }
  header {
    display: flex;
    flex-direction: column;
    gap: 1.25rem;
    align-items: center;
  }
  .socials {
    display: flex;
    width: 174px;
    padding-inline: 4px;
    justify-content: space-between;
  }

  a {
    cursor: pointer;
    z-index: 2;
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
</style>
