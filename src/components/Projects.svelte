<section>
  <div class="top-row">
    <h1>Projects</h1>
    <button>CONTACT ME</button>
  </div>
  <div class="project">
    <picture>
      <source
        media="(min-width:1200px)"
        srcset="images/thumbnail-project-1-large.webp"
      />
      <img
        src="images/thumbnail-project-1-small.webp"
        alt="project thumbnail"
        class="thumbnail"
      />
    </picture>

    <h3>DESIGN PORTFOLIO</h3>
    <ul class="tech-stack">
      <li>HTML</li>
      <li>CSS</li>
    </ul>
    <div class="buttons">
      <button>VIEW PROJECT</button>
      <button>VIEW CODE</button>
    </div>
  </div>
</section>

<style>
  section {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    margin-block: 80px;
  }

  .top-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .project {
    margin-block-start: 40px;
  }

  img.thumbnail {
    width: 345px;
    height: 253px;
  }

  ul.tech-stack {
    padding-block: 0.5rem;
    padding-inline: 0;
    margin: 0;
    list-style-type: none;
    color: var(--white);
    display: flex;
    gap: 18px;
  }

  .buttons {
    display: flex;
    gap: 2rem;
    padding-block: 20px;
  }
</style>
