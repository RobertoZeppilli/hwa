<script>
	import Timer from "./components/Timer.svelte";
	import HowTo from "./components/HowTo.svelte";

	let audio

	function timerEnds(e) {
		audio.play()
	}

	// let progress = 0
</script>

<main class="container">
	<div class="hand-washing-app">
		<h1>Hand-Washing App</h1>
		<Timer on:end={timerEnds}/>
		<HowTo />

		<h3>
			<a href="https://www.who.int/gpsc/clean_hands_protection/en/">
				Picture Source
			</a>

			<a href="https://freesound.org/people/metrostock99/sounds/345086/ ">
				Sound Source
			</a>
		</h3>

		<audio bind:this={audio}>
			<source src="sound.wav" />
		</audio>
	</div>
</main>

<style>
	.hand-washing-app {
		padding: 2.55rem;
		text-align: center;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}
</style>
