<script>
  let projects = [
    {
      name: "Design Portfolio",
      skills: ["HTML", "CSS"],
      thumbnailSmall: "images/thumbnail-project-1-small.webp",
      thumbnailLarge: "images/thumbnail-project-1-large.webp",
      projectLink: "/",
      githubLink: "/",
    },
    {
      name: "E-Learning Landing Page",
      skills: ["HTML", "CSS"],
      thumbnailSmall: "images/thumbnail-project-2-small.webp",
      thumbnailLarge: "images/thumbnail-project-2-large.webp",
      alt: "project thumbnail",
      projectLink: "/",
      githubLink: "/",
      isVisible: false,
    },
    {
      name: "Todo Web App",
      skills: ["HTML", "CSS", "Javascript"],
      thumbnailSmall: "images/thumbnail-project-3-small.webp",
      thumbnailLarge: "images/thumbnail-project-3-large.webp",
      alt: "project thumbnail",
      projectLink: "/",
      githubLink: "/",
      isVisible: false,
    },
    {
      name: "Entertainment Web App",
      skills: ["HTML", "CSS", "Javascript"],
      thumbnailSmall: "images/thumbnail-project-4-small.webp",
      thumbnailLarge: "images/thumbnail-project-4-large.webp",
      alt: "project thumbnail",
      projectLink: "/",
      githubLink: "/",
      isVisible: false,
    },
    {
      name: "Memory Game",
      skills: ["HTML", "CSS", "Javascript"],
      thumbnailSmall: "images/thumbnail-project-5-small.webp",
      thumbnailLarge: "images/thumbnail-project-5-large.webp",
      alt: "project thumbnail",
      projectLink: "/",
      githubLink: "/",
      isVisible: false,
    },
    {
      name: "Art Gallery Showcase",
      skills: ["HTML", "CSS", "Javascript"],
      thumbnailSmall: "images/thumbnail-project-6-small.webp",
      thumbnailLarge: "images/thumbnail-project-6-large.webp",
      alt: "project thumbnail",
      projectLink: "/",
      githubLink: "/",
      isVisible: false,
    },
  ];
</script>

<section>
  <div class="top-row">
    <h1>Projects</h1>
    <button>CONTACT ME</button>
  </div>
  {#each projects as project}
    <div class="project">
      <picture
        class={project.isVisible ? "hover" : ""}
        on:mouseover={() => (project.isVisible = true)}
        on:focus={() => (project.isVisible = true)}
        on:mouseleave={() => (project.isVisible = false)}
        on:blur={() => (project.isVisible = false)}
      >
        <source media="(min-width:1200px)" srcset={project.thumbnailLarge} />
        <img src={project.thumbnailSmall} alt={project.alt} />
      </picture>
      <h3>{project.name}</h3>

      <ul class="tech-stack">
        {#each project.skills as skill}
          <li>{skill}</li>
        {/each}
      </ul>
      <div
        class="buttons {project.isVisible ? 'show' : ''}"
        on:mouseover={() => (project.isVisible = true)}
        on:focus={() => (project.isVisible = true)}
        on:mouseleave={() => (project.isVisible = false)}
        on:blur={() => (project.isVisible = false)}
      >
        <button>VIEW PROJECT</button>
        <button>VIEW CODE</button>
      </div>
    </div>
  {/each}
</section>

<style>
  section {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    margin-block: 80px;
    align-items: center;
  }

  .top-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
  }

  .project {
    margin-block-start: 40px;
  }

  img {
    width: 345px;
    height: 253px;
  }

  h3 {
    padding-block-start: 20px;
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

  @media (min-width: 768px) {
    section {
      display: grid;
      grid-template-columns: 1fr 1fr;
      column-gap: 18px;
      row-gap: 2rem;
      padding-inline: 2rem;
      justify-items: center;
    }

    .top-row {
      grid-column: 1/3;
    }
    .project {
      position: relative;
    }

    img {
      width: 346px;
      height: 253px;
    }

    .buttons {
      display: flex;
    }
  }

  @media (min-width: 1200px) {
    picture {
      background: transparent;
    }
    picture.hover {
      opacity: 0.25;
      background: #000;
    }

    img {
      width: 540px;
      height: 400px;
    }

    .buttons {
      display: none;
      flex-direction: column;
      position: absolute;
      align-items: center;
      top: 20%;
      left: 35%;
    }

    .buttons.show {
      display: flex;
    }
  }
</style>
