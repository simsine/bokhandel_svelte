<script>

import Navbar from "../components/navbar.svelte"
import Bokseksjon from "../components/bokseksjon.svelte"
import bokdata from '../bokdata.json'

</script>

<!-- BODY -->

<Navbar />

<!--MAIN-->
<main>
    <h2 id="anbefalt">Anbefalt! - {bokdata.anbefalt.length} utvalgte titler</h2>
    <Bokseksjon bokliste={bokdata.anbefalt} />
    
    <h2 id="japansk">Japansk - {bokdata.japansk.length} utvalgte titler</h2>
    <Bokseksjon bokliste={bokdata.japansk} />
</main>

<style>
/* Roboto font */
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@500&display=swap');

:global(*){
    font-family: "Roboto", sans-serif;
}

/* Main */
main{
    margin: 15px;
}
main h2 {
    margin-top: 10px;
    margin-bottom: 10px
}
</style>