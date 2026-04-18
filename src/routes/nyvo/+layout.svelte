<script lang="ts">
	import { resolve } from '$app/paths';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href="/nyvo.svg" />
</svelte:head>

<nav
	class="fixed flex top-2 left-2 right-2 items-center justify-center h-12 border border-border rounded-lg p-2"
>
	<header class="flex items-center gap-1 basis-1/4 text-xl">
		<a href={resolve('/nyvo')}>
			<img src="/nyvo.svg" alt="Nyvo" class="h-8 ring ring-border rounded-sm" />
		</a>
		<a
			href={resolve('/')}
			class="font-bold ml-1 underline decoration-1 underline-offset-3 decoration-transparent hover:decoration-current"
			>Surreal</a
		>
		<a
			href={resolve('/nyvo')}
			class="underline decoration-1 underline-offset-3 decoration-transparent hover:decoration-current"
			>Nyvo</a
		>
	</header>
	<div class="basis-1/2"></div>
	<div class="basis-1/4"></div>
</nav>

<main>
	{@render children()}
</main>
