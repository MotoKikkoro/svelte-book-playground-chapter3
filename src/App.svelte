<script>
  let n =1;
  let stars;

  $: console.log ('nの値が${n}に変更されました')
  $: {
    const newStars = [];
    for (let i = 0; i <n; i++) {
      newStars.push(i % 2 === 0 ? '★' : '');
    }
    stars = newStars;
  }
</script>

<div>
  {#each stars as star}{star}{/each}
</div>

<div>
  <button on:click={()=> (n=n-1)} disabled={n<=1}>
    ★を減らす
    </button>
  
  <button on:click={()=> (n=n+1)}>
    ★を増やす
    </button>
</div>