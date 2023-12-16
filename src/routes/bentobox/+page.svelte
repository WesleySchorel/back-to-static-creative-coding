<script>
	import Heading from '$lib/components/heading.svelte';
	import walking from '$lib/assets/walking_together.svg';
	import knowledge from '$lib/assets/sharing_knowledge.svg';

	$: heading = { titel: 'Partners overzicht' };

	import { onMount } from 'svelte';

	let labelValue;
	let progressbar;

	// runs after the component is first rendered to the DOM.
	onMount(() => {
		let random = Math.floor(Math.random() * 100);

		progressbar.value = random;
		labelValue.innerHTML = random + '%';
	});
</script>

<Heading {heading} />

<div class="container">
	<div class="top">
		<a href="/gvb">
			<article>
				<h2>GVB</h2>
				<span>Laatst bewerkt: 12 min. geleden</span>
				<div class="progress-container">
					<progress id="progress-partner" max="100" value="0" bind:this={progressbar} />
					<label class="progress-percentage" for="progress-partner" bind:this={labelValue}>0%</label
					>
				</div>
			</article>
		</a>
		<a href="/gvb">
			<article>
				<h2>GVB</h2>
				<span>Laatst bewerkt: 12 min. geleden</span>
				<div class="progress-container">
					<progress id="progress-partner" max="100" value="0" bind:this={progressbar} />
					<label class="progress-percentage" for="progress-partner" bind:this={labelValue}>0%</label
					>
				</div>
			</article>
		</a>
		<a href="/gvb">
			<article>
				<h2>GVB</h2>
				<span>Laatst bewerkt: 12 min. geleden</span>
				<div class="progress-container">
					<progress id="progress-partner" max="100" value="0" bind:this={progressbar} />
					<label class="progress-percentage" for="progress-partner" bind:this={labelValue}>0%</label
					>
				</div>
			</article>
		</a>
		<a href="/gvb">
			<article>
				<h2>GVB</h2>
				<span>Laatst bewerkt: 12 min. geleden</span>
				<div class="progress-container">
					<progress id="progress-partner" max="100" value="0" bind:this={progressbar} />
					<label class="progress-percentage" for="progress-partner" bind:this={labelValue}>0%</label
					>
				</div>
			</article>
		</a>
	</div>
	<div class="middle">
		<a href="/gvb">
			<article>
				<h2>GVB</h2>
				<span>Laatst bewerkt: 12 min. geleden</span>
				<div class="progress-container">
					<progress id="progress-partner" max="100" value="0" bind:this={progressbar} />
					<label class="progress-percentage" for="progress-partner" bind:this={labelValue}>0%</label
					>
				</div>
			</article>
		</a>
		<a href="/gvb">
			<article>
				<h2>GVB</h2>
				<span>Laatst bewerkt: 12 min. geleden</span>
				<div class="progress-container">
					<progress id="progress-partner" max="100" value="0" bind:this={progressbar} />
					<label class="progress-percentage" for="progress-partner" bind:this={labelValue}>0%</label
					>
				</div>
			</article>
		</a>
	</div>
	<div class="bottom">
		<a href="/gvb">
			<article>
				<h2>GVB</h2>
				<span>Laatst bewerkt: 12 min. geleden</span>
				<div class="progress-container">
					<progress id="progress-partner" max="100" value="0" bind:this={progressbar} />
					<label class="progress-percentage" for="progress-partner" bind:this={labelValue}>0%</label
					>
				</div>
			</article>
		</a>
		<a href="/gvb">
			<article>
				<h2>GVB</h2>
				<span>Laatst bewerkt: 12 min. geleden</span>
				<div class="progress-container">
					<progress id="progress-partner" max="100" value="0" bind:this={progressbar} />
					<label class="progress-percentage" for="progress-partner" bind:this={labelValue}>0%</label
					>
				</div>
			</article>
		</a>
	</div>
	<div class="left">
		<a href="/gvb">
			<article>
				<h2>GVB</h2>
				<span>Laatst bewerkt: 12 min. geleden</span>
				<div class="progress-container">
					<progress id="progress-partner" max="100" value="0" bind:this={progressbar} />
					<label class="progress-percentage" for="progress-partner" bind:this={labelValue}>0%</label
					>
				</div>
			</article>
		</a>
	</div>
</div>

<style>
	@keyframes slideInTop {
		0% {
			transform: translateX(-100%);
		}
		100% {
			transform: translateX(0);
		}
	}

	@keyframes slideInMiddle {
		0% {
			transform: translateX(100%);
		}
		100% {
			transform: translateX(0);
		}
	}

	@keyframes slideInBottom {
		0% {
			transform: translateY(100%);
		}
		100% {
			transform: translateY(0);
		}
	}

	@keyframes slideInLeft {
		0% {
			transform: translateX(-100%);
		}
		100% {
			transform: translateX(0);
		}
	}

	.container {
		display: grid;
		grid-template-columns: 1fr 1fr 1fr;
		grid-template-rows: 1fr 1fr 1fr 1fr;
		grid-auto-columns: 1fr;
		gap: 0px 0px;
		grid-auto-flow: row;
		width: 99%;
		margin: 0 auto;
		margin-top: 2rem;
		overflow: hidden;
	}

	.top {
		grid-area: 1 / 1 / 3 / 4;
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		animation: slideInTop 1s ease-in-out;
	}

	.middle {
		grid-area: 2 / 2 / 4 / 4;
		display: grid;
		grid-template-columns: repeat(1, 1fr);
		animation: slideInMiddle 1s ease-in-out;
	}

	.bottom {
		grid-area: 4 / 2 / 5 / 4;
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		animation: slideInBottom 1s ease-in-out;
	}

	.left {
		grid-area: 3 / 1 / 5 / 2;
		display: grid;
		grid-template-columns: repeat(1, 1fr);
		animation: slideInLeft 1s ease-in-out;
	}

	article {
		background-color: var(--c-container);
		border: solid 1px var(--c-container-stroke);
		padding: 2rem 2rem 2rem 2rem;
	}

	a {
		margin: 0.5rem;
		text-decoration: none;
		color: var(--c-text);
	}

	a:hover {
		border: solid 1px var(--c-pink);
	}

	h2 {
		font-size: 1.5em;
		margin-top: 0.05em;
		margin-bottom: 2rem;
	}

	.left h2 {
		font-size: 1.5em;
		margin-top: 0.05em;
		margin-bottom: 14rem;
	}

	.progress-container {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		align-items: flex-end;
		gap: 1em;
		margin-top: 0.25em;
	}

	progress {
		width: 100%;
	}

	.progress-percentage {
		height: 85%;
	}
</style>
