<script>
	import Code from './+code.svelte';
	const zeropsyaml = `project:
   name: zerops-svelte

  services:
   - hostname: sveltenode
    type: nodejs@18
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
	<div class="grid grid-cols-1 xl:grid-cols-2 font-light gap-5 xl:gap-10 pt-4 px-36">
		<div class="bg-[#F7F7F7] rounded-md p-8 my-8 flex items-center">
			<div class="max-w-lg space-y-10">
				<div>
					<h3 class="font-semibold text-lg">Step 1</h3>
					<p class="font-medium">
						Go to{' '}
						<a href="https://app.zerops.io/dashboard/projects" target="_blank">
							Zerops Dashboard
						</a>{' '}
						and Click on the 'Import Project' button on the sidebar. (Not a user?{' '}
						<a href="https://zerops.io" target="_blank"> Register now </a>
						)
					</p>
				</div>
				<div>
					<h3 class="font-semibold text-lg">Step 2</h3>
					<p class="font-medium">
						Copy the YAML code mentioned here and paste it to import this example.
					</p>
					<p class="font-medium">
						Alternatively, you can clone zerops-solid-static to your GitHub profile and then replace
						the repository URL in the buildFromGit parameter.
					</p>
				</div>
			</div>
		</div>
		<Code code={zeropsyaml} />
	</div>
</div>
