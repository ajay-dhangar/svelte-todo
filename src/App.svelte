<script>
  import ToDo from "./ToDo.svelte";
  export let name;
</script>

<main>
  <h1>{name}</h1>
  <p>A simple todo list app built with Svelte</p>

  <!-- <p><a href="https://github.com/ajay-dhangar/svelte-todo">Visit my Svelte To Do Repo and give me ⭐!</a></p>
   -->

  <ToDo />
</main>

<!-- 
  <footer>
	<p>Made with ❤️ by <a href="https://github.com/ajay-dhangar">Ajay Dhangar</a>.</p>	
  </footer>
   -->

<style>
  :global(body) {
    background-color: rgb(81, 6, 81);
  }

  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
    color: #f5f5f5;
  }

  p {
    color: #def72c;
    font-size: 1.5rem;
  }

  /* footer {
	  margin-top: 1em;
	  text-align: center;
	  color: #f5f5f5;
	} */

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
