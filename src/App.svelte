<script>
  import Contact from "./components/Contact.svelte";
  import Intro from "./components/Intro.svelte";
  import Projects from "./components/Projects.svelte";
  import Skills from "./components/Skills.svelte";
  import Socials from "./components/Socials.svelte";
</script>

<main>
  <Intro />
  <Skills />
  <Projects />
  <Contact />
</main>

<style>
  main {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
</style>
