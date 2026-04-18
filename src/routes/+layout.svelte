<script lang="ts">
	import { resolve } from '$app/paths';
	import './layout.css';
	import { ModeWatcher } from 'mode-watcher';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href="/surreal.svg" />
</svelte:head>

<ModeWatcher />

<div class="bg-background text-foreground w-full min-h-screen">
	{@render children()}

	<footer class="text-center text-sm text-muted-foreground leading-8">
		&copy; 2026 Surreal Contributors / Leonard Lesinski
		<br />
		<a href={resolve('/imprint')} class="underline mr-1">Imprint</a> &bull;
		<a href={resolve('/privacy')} class="underline ml-1">Privacy Policy</a>
	</footer>
</div>
