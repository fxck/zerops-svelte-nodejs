<script lang="ts">
	import { writable } from 'svelte/store';

	export let code: string;

	const CopyIcon = `  <svg
    xmlns="http://www.w3.org/2000/svg"
    width="20"
    height="20"
    viewBox="0 0 24 24"
    fill="none"
    stroke="currentColor"
    strokeWidth="2"
    strokeLinecap="round"
    strokeLinejoin="round"
  >
    <rect x="9" y="9" width="13" height="13" rx="2" ry="2"></rect>
    <path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path>
  </svg>
`;

	const CheckIcon = `<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round">
      <polyline points="20 6 9 17 4 12"></polyline>
    </svg>`;

	let icon = writable(CopyIcon);

	const copy = async () => {
		await navigator.clipboard.writeText(code);
		icon.set(CheckIcon);
		setTimeout(() => icon.set(CopyIcon), 2000);
	};
</script>

<div class="bg-[#F7F7F7] rounded-md relative p-8 my-8 overflow-auto">
	<button
		on:click={copy}
		class="inline-flex items-center absolute justify-center top-4 right-4 p-2 rounded-md bg-[#e5704e] text-white"
	>
		{@html $icon}
	</button>

	<pre class="relative overflow-auto">
  <code class="text-[#585858] text-sm font-medium">{code}</code>
</pre>
</div>
