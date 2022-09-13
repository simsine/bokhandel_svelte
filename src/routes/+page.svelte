<script>

import Navbar from "../components/navbar.svelte"
import Bokseksjon from "../components/bokseksjon.svelte"

let anbefalt =
[
{
    tittel : "Fallteknikk",
    forfatter : "Inga H. Sætre",
    forsideBilde : "/src/media/bok1.png",
    beskrivelse : "En tegnet roman. Vi følger Rakel som flytter hjemmefra for å gå på videregåendeskole. En tett venninnegjeng som forsøksvis ønsker å spille i band og drive med kampsport i den alderen der verden skal oppdages.",
    merInfo : "Mer info",
},
{
    tittel : "MAUS - THE COMPLETE MAUS",
    forfatter : "Art Spiegelman",
    forsideBilde : "/src/media/bok2.png",
    beskrivelse : "The Complete Maus by Art Spiegelman - the Pulitzer prize-winning Holocaust survivor story 'The most affecting and successful narrative ever done about the Holocaust' Wall Street Journal"
},
{
    tittel : "MORT CINDER",
    forfatter : "Alberto Breccia",
    forsideBilde : "/src/media/bok3.png",
    beskrivelse : "lorem ipsum"
},
{
    tittel : "Brave New World",
    forfatter : "Aldous Huxley",
    forsideBilde : "/src/media/bok4.jpg",
    beskrivelse : " Largely set in a futuristic World State, whose citizens are environmentally engineered into an intelligence-based social hierarchy, the novel anticipates huge scientific advancements in reproductive technology, sleep-learning, psychological manipulation and classical conditioning.",
},
]

let japansk =
[
{
    tittel : "SUE & TAI-CHI 3",
    forfatter : "Forfatter",
    forsideBilde : "src/media/japansk1.png",
    beskrivelse : "Beskrivelse"
},
{
    tittel : "PRINCESS KNIGH",
    forfatter : "Forfatter",
    forsideBilde : "src/media/japansk2.png",
    beskrivelse : "Beskrivelse"
},
{
    tittel : "BOMBA",
    forfatter : "Forfatter",
    forsideBilde : "src/media/japansk3.png",
    beskrivelse : "Beskrivelse"
},
]

</script>

<!-- BODY -->

<Navbar />

<!--MAIN-->
<main>
    <h2 id="anbefalt">Anbefalt! - {anbefalt.length} utvalgte titler</h2>
    <Bokseksjon bokliste={anbefalt} />
    
    <h2 id="japansk">Japansk - {japansk.length} utvalgte titler</h2>
    <Bokseksjon bokliste={japansk} />
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