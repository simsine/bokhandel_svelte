<script>
  export let bokliste;

  // let filePath = "../src/media/"
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
      <!--Forsidebilde-->
      <a href="./boksider/"><img class="forsidebilde" src="{bok.forsideBilde}" alt=""></a>
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
      grid-template-columns: 80%;
      row-gap: 0.5rem;
    }
  }

  /* Cards */
  section article {
    width: 100%;
    padding: 5px;
    text-align: center;
  }

  section article .description {
    font-size: small;
    text-align: start;
  }

  section article a {
    background-color: lightgray;
  }
  section article .forsidebilde {
    width: 90%;
    box-shadow: 3px 5px 5px 0 rgb(0 0 0 / 16%), 0 2px 10px 0 rgb(0 0 0 / 12%);
  }
</style>
