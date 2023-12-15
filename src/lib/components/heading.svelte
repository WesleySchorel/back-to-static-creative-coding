<script>
	export let heading;
	import arrowRight from '$lib/assets/Blocks.svg';

	const faviconAPI =
		'https://t1.gstatic.com/faviconV2?client=SOCIAL&type=FAVICON&fallback_opts=TYPE,SIZE,URL&url=';
</script>

<section>
	<div class="container">
		<div class="text">
			<h1>
				{heading.titel}{#if heading.url}/{heading.url}{/if}
			</h1>
			<p>
				Bekijk alles over {heading.titel}{#if heading.url}/{heading.url}{/if} met de Tool van Vervoerregio Amsterdam in een overzicht. 
			</p>
		</div>
		<div class="media">
			<img src={arrowRight} alt="Blocks"/>
		</div>
	</div>
</section>

<style>
	/* container heading 1 */
	section {
		display: flex;
		gap: 1rem;
		align-items: center;
		background-color: var(--c-container);
		padding: 4em;
		border-top: 12px solid var(--c-pink);
		margin: 1em 1em;
		border-radius: 0.5em;
	}

	.container {
		display: grid;
		grid-template-columns: 1fr 1fr;
		grid-template-rows: 1fr;
		grid-auto-columns: 1fr;
		gap: 0px 0px;
		grid-auto-flow: row;
		grid-template-areas: 'text media';
	}

	.media {
		grid-area: media;
		padding: 1rem;
	}

	.media img {
		width: 75%;
		height: auto;
	}

	.text {
		grid-area: text;
		padding: 1rem;
	}

	h1 {
		font-size: 5rem;
	}

	p {
		font-size: 1.5rem;
	}
</style>