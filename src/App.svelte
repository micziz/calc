<script>
	let num1;
	let num2;
  let op;
  let res = ''

  function handleSubmit(){
    res = eval(`${num1} ${op} ${num2}`)
    return res;
  }
</script>

<h1 class="title is-1" style="text-align: center; margin-top: 2rem;">Calc</h1>


<div>
  <form action="" on:submit|preventDefault={handleSubmit}>
    <div id="formDiv-1">
      <input type="text" id="num1" bind:value={num1} placeholder="First Number" style="margin-right: 2rem;">
      <input type="text" id="num2" bind:value={num2} placeholder="Second Number">
    </div>
    <div id="dataList">
      <input list="op" bind:value={op}>
      <datalist id="op">
        <option value="+">
        <option value="-">
        <option value="*">
        <option value="/">
      </datalist>
    </div>
    <div id="submit">
      <input type="submit" class="button is-link is-outlined" value="Calculate">
    </div>
  </form>
</div>

<p id="res">
  {res}
</p>

<style>
  @import "https://cdn.jsdelivr.net/npm/bulma@0.9.4/css/bulma.min.css";

  #formDiv-1{
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  #dataList{
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 3rem;
  }

  #submit{
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 3rem;
  }

  #res{
    text-align: center;
    margin-top: 2rem;
    font-size: xx-large;
  }
</style>