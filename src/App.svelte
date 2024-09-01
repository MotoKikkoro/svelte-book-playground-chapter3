<script>
  let n =1;
  $: if (n>10) {
    alert ('数量多すぎ。10個以内にしてください');
    n=10;
  }
  </script>

  <div>
    数量 : {n}
  </div>

  <div>
    <button on:click={()=> (n=n-1)} disabled={n<=1} >減らす
    </button>
    <button on:click={()=> (n=n+1)} >増やす
    </button>
  
  </div>