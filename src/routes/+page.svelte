<script lang="ts">
	import Typewriter from 'svelte-typewriter'
import Background from './components/background.svelte';
	import WipNotification from './components/wipNotification.svelte';
</script>

<main>
	<WipNotification />
	<div class="hero min-h-screen bg-base-200">
		<div class="hero-content text-center">
			<div class="max-w-md">
				<h1 class="text-5xl font-bold">
          <Typewriter keepCursorOnFinish={true} interval={50}>
            <h1>Wavelink</h1>
          </Typewriter>
        </h1>
				<p class="py-6">
					Young and curious self-taught full-stack developer and student from the Czech Republic.
				</p>
				<button class="btn btn-primary">Learn more</button>
			</div>
		</div>
	</div>
</main>
