<script>
    import { svg } from "d3";

  let numbers= [10,25,33,62,75,100]

</script>

<h1> Rendimiento de la batería durante el día</h1>

<div class="col-container">
  {#each numbers as n}
      <div class="col-wrapper">
        {#if n > 30}
          <div class="column verde" style="height: {n * 162 / 100}px;"> </div>
        {:else}
          <div class="column rojo" style="height: {n * 162 / 100}px;"> </div>
        {/if}
        <img class="mask" src="./images/Union.svg" alt="">
      </div>
  {/each}
</div>

<style>

  .col-container{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: row-reverse;
    margin-top: 0;
  }

  .col-wrapper{
    position: relative;
    width: 60px;
    margin-top: 0px;
    height: 100px;
    margin: 50px;
  }

  .column{    /* relleno de columnas */
    position: absolute;
    width: 65px;
    bottom: -39px;
    left:0.2px;   
  }

  .verde{
    background-color:green;
  }

  .rojo{
    background-color: red;
  }

  .mask{
    position:relative;
    width:75px;
    bottom: 35px;
    right: 5px;
    z-index: 1;
  }

  h1{
    font-family: 'Poppins', sans-serif;
    font-size: 65px;
    margin-top: 200px;
    text-align: center;
  }

</style>