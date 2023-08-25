<script lang='ts'>
	// The ordering of these imports is critical to your app working properly
	import '@skeletonlabs/skeleton/themes/theme-hamlindigo.css';
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/skeleton.css';
	// Most of your app wide CSS should be put in this file
	import '../app.postcss';
	import { AppShell, AppBar, Drawer, drawerStore } from '@skeletonlabs/skeleton';
	import Navigation from '$lib/Navigation.svelte';
	function drawerOpen(): void{
		drawerStore.open();
	}
</script>
<Drawer>
	<Navigation />
</Drawer>

<!-- App Shell -->
<AppShell slotSidebarLeft="w-0 md: w-52 bg-surface-500/10 p-4">
	<svelte:fragment slot="header">
		<!-- App Bar -->
		<AppBar>
			<svelte:fragment slot="lead">
				<button class="md:hissen btn btn-sm mr-4" on:click={drawerOpen}>
					<span>
						<svg viewBox="0 0 100 80" class="fill-token w-4 h-4">
							<rect width="100" height="20"></rect>
							<rect y="30" width="100" height="20"></rect>
							<rect y="60" width="100" height="20"></rect>
						</svg>
					</span>
				</button>
				<strong class="p-10 text-xl uppercase">FUTURE</strong>
			</svelte:fragment>
			<svelte:fragment slot="trail">
				<header>
					<nav>
						<ul class="flex space-x-4">
							<li>
								<a href="/" class="block px-2 py-1">Home</a>
							</li>
							<li>
								<a href="/about" class="block px-2 py-1">About</a>
							</li>
							<li>
								<a href="/sites" class="block px-2 py-1">Sites</a>
							</li>
							<li>
								<a href="/Random" class="block px-2 py-1">Random</a>
						</ul>
					</nav>
				</header>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<!-- Page Route Content -->
	<div class="container p-3 mx-auto">
		<slot />
	</div>
</AppShell>
