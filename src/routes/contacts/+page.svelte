<script lang="ts">
	import Typewriter from 'svelte-typewriter';
	import { copyTextToClipboard } from '../../clipboard';

	function openInNewTab(link: string) {
		window.open(link, '_blank');
	}
</script>

<main class="flex justify-center align-middle flex-col text-center">
	<div class="text-5xl mt-20">
		<Typewriter cursor={true} keepCursorOnFinish={true}><h1>About</h1></Typewriter>
	</div>
	<div class="inline-block">
		<span class="text-2xl">Email: </span>
		<div class="dropdown dropdown-right">
			<label tabindex="0" class="btn m-1">wavelink@email.cz</label>
			<ul tabindex="0" class="dropdown-content menu p-2 shadow bg-base-100 rounded-box w-52">
				<li><a href="mailto:wavelink@email.cz">Send email</a></li>
				<li><a href="" on:click={() => copyTextToClipboard('wavelink@email.cz')}>Copy</a></li>
			</ul>
		</div>
	</div>

	<div class="inline-block">
		<span class="text-2xl">Discord: </span>
		<div class="dropdown dropdown-right">
			<label tabindex="0" class="btn m-1">Wavelink#5298</label>
			<ul tabindex="0" class="dropdown-content menu p-2 shadow bg-base-100 rounded-box w-52">
				<li><a href="" on:click={() => copyTextToClipboard('Wavelink#5298')}>Copy</a></li>
			</ul>
		</div>
	</div>

	<div class="inline-block">
		<span class="text-2xl">Github: </span>
		<div class="dropdown dropdown-right">
			<label tabindex="0" class="btn m-1">Wavelinkdev</label>
			<ul tabindex="0" class="dropdown-content menu p-2 shadow bg-base-100 rounded-box w-52">
				<li><a on:click={() => {openInNewTab("https://github.com/WaveLinkdev")}}>Open in new tab</a></li>
				<li>
					<a href="" on:click={() => copyTextToClipboard('https://github.com/WaveLinkdev')}>Copy</a>
				</li>
			</ul>
		</div>
	</div>
</main>
