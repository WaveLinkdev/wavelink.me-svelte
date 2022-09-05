<script lang="ts">
	import Navigation from '../components/navigation.svelte';
	import Typewriter from 'svelte-typewriter';
	import Background from '../components/background.svelte';
	import { onMount } from 'svelte';
	import { Icon } from '@steeze-ui/svelte-icon';
	import {
		Go,
		Nodedotjs,
		Csharp,
		Html5,
		Css3,
		Javascript,
		React,
		Svelte,
		Nextdotjs,
		Unity,
		Typescript,
		Python,
		Assemblyscript,
		Dotnet,
		Blazor,
		Webstorm,
		Rider,
		Datagrip,
		Visualstudio,
		Visualstudiocode,
		Gitkraken,
		Linux,
		Archlinux,
		Ubuntu,
		Powershell,
		Windows,
		Git,
		Github,
		Gitlab,
		Mongodb,
		Mysql,
		Sqlite,
		Redis,
		Prisma,
		Tailwindcss,
		Bootstrap,
		Prettier,
		Eslint,
		Vite,
		Pnpm,
		Arduino,
		Autohotkey,
		Blender,
		Jetbrains
	} from '@steeze-ui/simple-icons';

	export const prerender = true;
</script>

<main class="flex justify-center align-middle flex-col text-center">
	<div class="text-5xl mt-20">
		<Typewriter cursor={true} keepCursorOnFinish={true}><h1>About</h1></Typewriter>
	</div>
	<div class="w-full flex justify-center">
		<div
			tabindex="0"
			class="collapse collapse-plus border border-base-300 bg-base-100 rounded-box mt-10 w-7/12"
		>
			<input type="checkbox" />
			<div class="collapse-title text-xl font-medium">All tools</div>
			<div class="collapse-content">
				<div class="">
					<div>
						<p>Languages:</p>
						<ul>
							<Icon src={Javascript} size="2em" class="inline-block fill-yellow-400" />
							<Icon src={Typescript} size="2em" class="inline-block fill-blue-600" />
							<Icon src={Assemblyscript} size="2em" class="inline-block fill-blue-600" />
							<Icon src={Csharp} size="2em" class="inline-block fill-purple-700" />
							<Icon src={Go} size="2em" class="inline-block fill-blue-700" />
							<Icon src={Python} size="2em" class="inline-block fill-blue-400" />
							<Icon src={Html5} size="2em" class="inline-block fill-orange-700" />
							<Icon src={Css3} size="2em" class="inline-block fill-blue-700" />
						</ul>
					</div>
					<div>
						<p>Frameworks:</p>
						<ul>
							<Icon src={Svelte} size="2em" class="inline-block fill-red-600" />
							<Icon src={React} size="2em" class="inline-block fill-blue-600" />
							<Icon src={Nextdotjs} size="2em" class="inline-block fill-black" />
							<Icon src={Nodedotjs} size="2em" class="inline-block fill-green-600" />
							<Icon src={Dotnet} size="2em" class="inline-block fill-blue-600" />
							<Icon src={Blazor} size="2em" class="inline-block fill-purple-600" />
							<Icon src={Unity} size="2em" class="inline-block fill-black" />
						</ul>
					</div>
					<div>
						<p>Tools:</p>
						<ul>
							<Icon src={Webstorm} size="2em" class="inline-block fill-blue-600" />
							<Icon src={Rider} size="2em" class="inline-block fill-purple-400" />
							<Icon src={Datagrip} size="2em" class="inline-block fill-purple-200" />
							<Icon src={Visualstudio} size="2em" class="inline-block fill-purple-600" />
							<Icon src={Visualstudiocode} size="2em" class="inline-block fill-blue-600" />
							<Icon src={Gitkraken} size="2em" class="inline-block fill-green-300" />
						</ul>
					</div>
					<div>
						<p>Librarires:</p>
						<ul>
							<Icon src={Prisma} size="2em" class="inline-block fill-white" />
							<Icon src={Tailwindcss} size="2em" class="inline-block fill-blue-600" />
							<Icon src={Bootstrap} size="2em" class="inline-block fill-purple-600" />
							<Icon src={Prettier} size="2em" class="inline-block fill-gray-600" />
							<Icon src={Eslint} size="2em" class="inline-block fill-purple-600" />
							<Icon src={Vite} size="2em" class="inline-block fill-yellow-600" />
							<Icon src={Pnpm} size="2em" class="inline-block fill-yellow-600" />
						</ul>
					</div>
					<div>
						<p>Databases:</p>
						<ul>
							<Icon src={Mongodb} size="2em" class="inline-block fill-green-600" />
							<Icon src={Mysql} size="2em" class="inline-block fill-blue-600" />
							<Icon src={Sqlite} size="2em" class="inline-block fill-blue-600" />
							<Icon src={Redis} size="2em" class="inline-block fill-red-600" />
						</ul>
					</div>
					<div>
						<p>Version Control:</p>
						<ul>
							<Icon src={Git} size="2em" class="inline-block fill-red-600" />
							<Icon src={Github} size="2em" class="inline-block fill-gray-600" />
							<Icon src={Gitlab} size="2em" class="inline-block fill-orange-600" />
						</ul>
						<div />
						<div>
							<p>Operating Systems:</p>
							<ul>
								<Icon src={Linux} size="2em" class="inline-block fill-black" />
								<Icon src={Archlinux} size="2em" class="inline-block fill-blue-400" />
								<Icon src={Ubuntu} size="2em" class="inline-block fill-orange-600" />
								<Icon src={Windows} size="2em" class="inline-block fill-blue-600" />
							</ul>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</main>
