<script>
	export let bokliste;
</script>

<!-- BODY -->
<h2 class="section-heading">{bokliste.seksjonHeading} - {bokliste.bøker.length} utvalgte titler</h2>
<section id="{bokliste.seksjonHeading}">
	{#each bokliste.bøker as bok}
	<article>
		<!--Forsidebilde-->
		<a href="."><img class="bok-forsidebilde" src="{bok.forsideBilde}" alt=""></a>
		<!--Tittel-->
		<h3 class="bok-tittel">{bok.tittel}</h3>
		<!--Forfatter-->
		<a href="http://" target="_blank">
			<p class="bok-forfatter">{bok.forfatter}</p>
		</a>
		<!--Beskrivelse-->
		<p class="bok-beskrivelse">{bok.beskrivelse}</p>
	</article>
	{/each}
</section>
<hr>
<!-- END OF BODY -->
<style>
	/* Section */
	.section-heading {
		margin-top: 10px;
		margin-bottom: 10px
	}
	section {
		margin-top: 15px;
		margin-bottom: 15px;
		display: grid;
		grid-template-columns: repeat(4, 20%);
		justify-items: center;
		justify-content: space-around;
		gap: 1rem;
		row-gap: 1rem;
	}

	/* Cards */
	section article {
		display: flex;
		flex-direction: column;
		width: 100%;
		padding: 15px;
		text-align: left;

		background-color: rgb(241,245,243);
		border-radius: 0.5rem;
	}
	.bok-tittel, .bok-forfatter, .bok-beskrivelse{
		margin-top: 0.75rem;
		margin-bottom: 0rem;
	}
	.bok-beskrivelse {
		font-size: small;
		text-align: start;
	}
	.bok-beskrivelse::before{
		content: '«';
	}
	.bok-beskrivelse::after{
		content: '»';
	}
	.bok-forsidebilde {
		justify-self: center;
		width: 100%;

		border-radius: 0.5rem;
		box-shadow: 3px 5px 5px 0 rgb(0 0 0 / 16%), 0 2px 10px 0 rgb(0 0 0 / 12%);
	}

	/* Media queries */
	@media screen and (min-width: 550px) and (max-width: 900px) {
		section {
			grid-template-columns: repeat(3, 30%);
			row-gap: 0.5rem;
		}
	}
	@media screen and (max-width: 550px) {
		section {
			grid-template-columns: 85%;
			row-gap: 1rem;
		}
		section article {
			padding: 30px;
		}
	}
</style>