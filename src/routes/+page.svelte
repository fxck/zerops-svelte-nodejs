<script>
	import SvelteLogo from '../lib/assets/svelte.svg';
	import ZeropsLogo from '../lib/assets/zerops.svg';
	import Steps from '../components/+steps.svelte';
	import Register from '../components/+register.svelte';
</script>

<div class=" justify-center py-10">
	<div class="text-center py-20">
		<div class="flex flex-row justify-center space-x-32">
			<img src={SvelteLogo} width="100px" draggable="false" alt="download icon" />
			<img src={ZeropsLogo} width="100px" draggable="false" alt="download icon" />
		</div>
		<h1 class="text-6xl font-extrabold space-y-3 mt-6 mb-6 leading-normal mt-8">
			Say Hello to <span class="block"
				><span class="text-[#FF3E00]">SvelteKit</span>{' '}+ Zerops</span
			>
		</h1>
		<p class="font-semibold max-w-[800px] mx-auto text-2xl">
			A Static Remix example for Zerops which you can deploy in 2 simple steps (Technically, we
			don't count Ctrl + V... but who's checking?). Scroll down to learn how to deploy.
		</p>
		<div class="mt-10 flex text-lg flex-row justify-center items-center space-x-5">
			<a href="https://discord.gg/5ptAqtpyvh" target="_blank">
				<button class="primarybutton rounded-md"> Discord Community </button>{' '}
			</a>
			<a href="https://docs.zerops.io/" target="_blank">
				<button class="secondarybutton rounded-md"> Zerops Docs </button>
			</a>
		</div>
	</div>
	<div class="flex justify-center pt-14">
		<Steps />
	</div>
	<p class="text-center mt-10 text-[#939393]">
		Powered by{' '}
		<a href="https://zerops.io" target="_blank"> Zerops </a>
	</p>
	<Register />
</div>

<style>
	@import '../main.css';
</style>
