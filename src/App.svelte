<script>
  let range = {min:0, max:5};
  let values =[];

  $: {
    const newValues = [];
    for (let i = range.min; i <= range.max; i++) {
      newValues.push(i);
    }
    values = newValues;
  }

  function handleMinChange(event) {
    range.min =parseInt(event.target.value);
  }

  function handleMaxChange(event){
    range.max = parseInt(event.target.value);
  }
</script>

<div>
  <input type="number" min={0} max ={range.max} value={range.min} on:change={handleMinChange}>
  <input type="number" min={range.min} max ={100} value={range.max} on:change={handleMaxChange}>
</div>

{#each values as value}
<button>value</button>
{/each}