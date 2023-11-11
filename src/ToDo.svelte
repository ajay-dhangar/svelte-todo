<script>

  let todos = [];
  let newTodo = '';


  function addTodo() {
    todos = [...todos, { id: Date.now(), text: newTodo }];
    newTodo = '';
  }


  function removeTodo(id) {
    todos = todos.filter(todo => todo.id !== id);
  }
</script>


<main>
 
  <h1>Svelte Todo List</h1>


  <input bind:value={newTodo} placeholder="Add a new todo" />


  <button on:click={addTodo}>Add</button>

  <!-- List of todos -->
  <ul>
    {#each todos as { id, text }}

      <li key={id}>
        {text} <button on:click={() => removeTodo(id)}>Remove</button>
      </li>
    {/each}
  </ul>
</main>


<style>

  main {
    text-align: center;
    margin-top: 50px;
  }

  ul {
    list-style: none;
    padding: 0;
  }

  li {
    margin: 10px 0;
  }
</style>
