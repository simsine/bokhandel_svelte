<script>
  export let bokliste;
</script>

<section id="section-anbefalt">
  {#each bokliste as bok}
    <article>
      <!--Tittel-->
      <h1>{bok.tittel}</h1>
      <!--Forfatter-->
      <a href="http://" target="_blank">
        <p>{bok.forfatter}</p>
      </a>
      <!--Forsidebilde TODO-->
      <div><a href="./boksider/"><img src={bok.forsideBilde} alt="" /></a></div>
      <!--Beskrivelse-->
      <p class="description">{bok.beskrivelse}</p>
      <!--Mer info-->
      <a href="http://" target="_blank">
        <p>{bok.merInfo}</p>
      </a>
    </article>
  {/each}
</section>

<style>
  section {
    display: grid;
    grid-template-columns: repeat(4, 20%);
    justify-items: center;
    justify-content: space-around;
    gap: 1rem;
  }

  @media screen and (max-width: 480px) {
    section {
      grid-template-columns: 75%;
      row-gap: 0.5rem;
    }
  }

  /* Cards */
  section article {
    padding: 5px;
    /* min-width: 250px; */
    /* border: 1px solid black; */
    text-align: center;
  }

  section article .description {
    font-size: small;
    text-align: start;
  }

  section article img {
    box-shadow: 3px 5px 5px 0 rgb(0 0 0 / 16%), 0 2px 10px 0 rgb(0 0 0 / 12%);
    
  }
</style>
