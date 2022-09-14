<script>
	import Navbar from "../components/navbar.svelte"
	import Bokseksjon from "../components/bokseksjon.svelte"
	import bokdata from '../bokdata.json'
</script>

<!-- BODY -->

<Navbar />

<!--MAIN-->
<main>
    <Bokseksjon bokliste={bokdata.anbefalt} />
    <Bokseksjon bokliste={bokdata.japansk} />
</main>

<!-- footer? -->

<style>
/* Roboto font */
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@500&display=swap');
:global(*){
    font-family: "Roboto", sans-serif;
}
/* Reset body */
:global(body) {
		margin: 0;
	}

/* Main */
main{
    margin: 15px;
}
</style>