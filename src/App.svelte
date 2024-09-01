<script>
  let todos =[];
  function handleClick(){
    todos.push('新しいtodo');
    todos = todos;
}
</script>

<ul>
  {#each todos as todo}
  <li>{todo}</li>
  {/each}
</ul>

<button on:click={handleClick}>追加</button>