<script>
  let todos =[];
  function handleClick(){
    todos = [...todos, ('新しいtodo')];
}
</script>

<ul>
  {#each todos as todo}
  <li>{todo}</li>
  {/each}
</ul>

<button on:click={handleClick}>追加</button>