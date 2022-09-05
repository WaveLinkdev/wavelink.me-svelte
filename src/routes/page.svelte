<script>
	import Background from './components/background.svelte';
	import { onMount } from 'svelte';
	import { debug } from 'svelte/internal';

  import Typewriter from 'svelte-typewriter'
	import Navigation from './components/navigation.svelte';

	export let title = '';
	var titles = [
		'Wavelink',
		'function Wavelink() {}',
		'const Wavelink = 1',
		'Wavelink = () => {}',
		'UInt16 Wavelink = 1'
	];

	var lastTitle = 0;

	onMount(() => {
    setInterval(() => {
      lastTitle++;
      if (lastTitle >= titles.length) {
        lastTitle = 0;
      }
      title = titles[lastTitle];
    }, 3000);
  });
</script>

<main class="flex justify-center text-center">
  <Background />
	<!-- <Navigation /> -->
	<div>
		<div class="text-5xl text-zinc-300">
			<Typewriter mode="loop">
        <h1>Wavelink</h1>
        <h1>Wavelink()</h1>
        <h1>const Wavelink</h1>
      </Typewriter>
		</div>
		<p>A self-taught developer and student from the Czech Republic.</p>
		<p>
			<a href="/about.html">Learn more</a>
		</p>
		<p>
			<a href="https://github.com/wavelinkdev/wavelink.me">Source code for this website</a>
		</p>
	</div>
</main>

<!-- <style>
	main {
		display: flex;
		justify-content: center;
		flex-direction: column;
	}

	h1 {
		font-weight: lighter;
		font-size: 2em;
		margin: 0;
		margin-top: 50px;
		text-align: start;
	}


	@keyframes slide {
		0% {
			transform: translateX(-100%);
		}

		100% {
			transform: none;
		}
	}
</style>
 -->