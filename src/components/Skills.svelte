<hr class="tablet-hr" />
<section>
  <hr />
  <div class="skill">
    <h2>HTML</h2>
    <p>4 Years Experience</p>
  </div>
  <div class="skill">
    <h2>CSS</h2>
    <p>4 Years Experience</p>
  </div>
  <div class="skill">
    <h2>Javascript</h2>
    <p>4 Years Experience</p>
  </div>
  <div class="skill">
    <h2>Accessibility</h2>
    <p>4 Years Experience</p>
  </div>
  <div class="skill">
    <h2>React</h2>
    <p>3 Years Experience</p>
  </div>
  <div class="skill">
    <h2>Sass</h2>
    <p>3 Years Experience</p>
  </div>
  <hr />
</section>

<style>
  section {
    display: flex;
    flex-direction: column;
    gap: 24px;
    align-items: center;
    text-align: center;
    width: 100%;
    margin-block-start: 80px;
  }

  div.skill:first-of-type {
    padding-block-start: 40px;
  }

  div.skill:last-of-type {
    padding-block-end: 40px;
  }

  hr.tablet-hr {
    display: none;
  }

  @media (min-width: 768px) {
    section {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 3rem;
      position: relative;
      text-align: start;
      padding-inline: 2rem;
      margin-block: 0;
    }

    h2 {
      font-size: 48px;
    }

    section::before {
      background: var(--white);
      height: 1px;
      width: 100%;
      position: absolute;
    }

    div.skill:first-of-type {
      padding-block-start: 0;
    }

    div.skill:last-of-type {
      padding-block-end: 0;
    }

    hr.tablet-hr {
      display: block;
      margin-block: 3rem;
    }
    hr:not(.tablet-hr) {
      display: none;
    }
  }
</style>
