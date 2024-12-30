<script>
  let name = "distoni";
  let profession = "Web and Software Developer";
  let skills = ["HTML", "TypeScript", "Java", "Svelte", "Kotlin", "Node.js"];
  let imageUrl = "https://files.catbox.moe/yn9cgp.png";

  import { onMount } from "svelte";
  onMount(() => {
    document.body.classList.add("dark");
  });
</script>

<main>
  <section class="home">
    <div class="profile">
      <img src={imageUrl} alt="Your Name" class="profile-image" />
      <div class="profile-text">
        <h1>{name}</h1>
        <p>{profession}</p>
      </div>
    </div>
  </section>

  <section class="skills">
    <h2>Skills</h2>
    <ul>
      {#each skills as skill}
        <li>{skill}</li>
      {/each}
    </ul>
  </section>

  <footer>
    <div class="links">
      <a href="https://github.com/distoni" target="_blank" class="link">GitHub</a>
      <a href="https://modrinth.com/user/diston1" target="_blank" class="link">Modrinth</a>
    </div>
    <p>Made with ❤️ using Svelte</p>
  </footer>
</main>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    font-family: 'Arial', sans-serif;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    transition: background-color 0.3s, color 0.3s;
  }

  body.dark {
    background-color: #242323dc;
    color: #242323dc;
  }

  main {
    padding: 20px;
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    text-align: center;
  }

  .home {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-bottom: 40px;
  }

  .profile {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }

  .profile-image {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    margin-bottom: 20px;
  }

  .profile-text {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  h1 {
    font-size: 3rem;
    margin-bottom: 10px;
  }

  p {
    font-size: 1.5rem;
    color: #555;
  }

  .skills {
    margin-top: 40px;
    margin-bottom: 40px;
  }

  .skills h2 {
    font-size: 2rem;
    margin-bottom: 20px;
  }

  .skills ul {
    list-style-type: none;
  }

  .skills li {
    margin-bottom: 10px;
    font-size: 1.2rem;
  }

  footer {
    text-align: center;
    margin-top: 40px;
    font-size: 1rem;
  }

  .links {
    margin-bottom: 10px;
  }

  .link {
    font-size: 1.2rem;
    margin-right: 15px;
    color: #0077b5;
    text-decoration: none;
  }

  .link:hover {
    text-decoration: underline;
  }
</style>
