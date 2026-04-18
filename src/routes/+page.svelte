<script lang="ts">
	import * as Item from '$ui/item';
	import ChevronRight from '@lucide/svelte/icons/chevron-right';
	import { resolve } from '$app/paths';
</script>

<svelte:head>
	<title>Surreal</title>
</svelte:head>

<div class="w-full min-h-screen flex items-center justify-center flex-col">
	<div class="flex items-center gap-6 mb-12">
		<img src="/surreal.svg" alt="Surreal icon" class="h-22 rounded-2xl border-border border" />
		<h1 class="font-semibold text-6xl">Surreal</h1>
	</div>
	<p class="text-xl mb-4">our projects</p>
	<div class="flex w-full max-w-md flex-col gap-4">
		<Item.Root variant="outline">
			{#snippet child({ props })}
				<a href={resolve('/nyvo')} {...props}>
					<Item.Media variant="image">
						<img
							src="/nyvo.svg"
							alt="Nyvo"
							width="32"
							height="32"
							class="size-8 rounded-lg object-cover border-border border"
						/>
					</Item.Media>
					<Item.Content>
						<Item.Title class="line-clamp-1">Nyvo</Item.Title>
						<Item.Description>File Compression & Archiving Tool</Item.Description>
					</Item.Content>
					<Item.Content class="flex-none text-center">
						<Item.Description><ChevronRight /></Item.Description>
					</Item.Content>
				</a>
			{/snippet}
		</Item.Root>
	</div>
</div>
