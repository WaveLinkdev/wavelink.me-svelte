<script>
	import { Icon } from '@steeze-ui/svelte-icon';
	import { Info } from '@steeze-ui/css-gg';
	import { onMount } from 'svelte';
	import { tweened } from 'svelte/motion';
	import { cubicInOut } from 'svelte/easing';

	let position = tweened(-100, { duration: 1000, easing: cubicInOut });

	onMount(() => {
		position.set(0);
		const timeout = setTimeout(() => {
			position.set(-100);
      clearTimeout(timeout);
		}, 3500);
	});
</script>

<div class="w-full m-5 fixed flex justify-center align-middle z-20" style={`top: ${$position}px`}>
	<div class="alert alert-info shadow-lg bg-opacity-50 w-11/12">
		<div>
			<Icon src={Info} size="24" />
			<span>This website is still under development</span>
		</div>
	</div>
</div>
