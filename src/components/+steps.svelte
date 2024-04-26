<script>
	import Code from './+code.svelte';
	const zeropsyaml = `project:
   name: zerops-svelte

  services:
   - hostname: sveltenode
    type: nodejs@20
    buildFromGit: https://github.com/fxck/zerops-svelte-nodejs
    ports:
      - port: 3000
        httpSupport: true
    enableSubdomainAccess: true
    minContainers: 1`.trim();
</script>

<div>
	<hr class="py-6 border-[#f4f4f4]" />
	<h2 class="text-center text-4xl font-semibold text-[#333]">Instructions</h2>
	<div class="grid grid-cols md:grid-cols-2 font-light gap-5 md:gap-10 pt-4">
		<div class="bg-[#F7F7F7] rounded-md p-8 my-8 flex items-center">
			<div class="max-w-lg space-y-10">
				<div>
					<h3 class="font-semibold text-lg">Step 1</h3>
					<!-- svelte-ignore a11y-media-has-caption -->
					<video width="full" class="rounded-xl mt-3" autoplay loop>
						<source src="import.mp4" type="video/mp4" />
					</video>
					<p class="font-medium mt-3">
						<a href="https://zerops.io" target="_blank"> Create an account </a>{' '}
						and locate the import button as shown in the video.
					</p>
				</div>
			</div>
		</div>
		<div class="flex flex-col">
			<div class="bg-[#F7F7F7] rounded-md p-8 my-8 flex items-center">
				<div class="max-w-lg space-y-10">
					<div>
						<h3 class="font-semibold text-lg">Step 2</h3>
						<p class="font-medium">Copy and paste the YAML code and confirm</p>
					</div>
				</div>
			</div>
			<Code code={zeropsyaml} />
		</div>
	</div>
</div>
