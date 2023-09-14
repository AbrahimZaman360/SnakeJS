<script lang="ts">
	import '../app.postcss';
	import { AppShell, AppBar, LightSwitch } from '@skeletonlabs/skeleton';

	// Floating UI for Popups
	import { computePosition, autoUpdate, flip, shift, offset, arrow } from '@floating-ui/dom';
	import { storePopup } from '@skeletonlabs/skeleton';
	storePopup.set({ computePosition, autoUpdate, flip, shift, offset, arrow });
</script>

<svelte:head>
	<title>SnakeTS</title>
	<meta name="description" content="SnakeTS" />
	<meta name="viewport" content="width=device-width, initial-scale=1" />
	<meta name="robots" content="index, follow" />
	<meta property="og:type" content="website" />
	<meta property="og:site_name" content="SnakeTS" />
	<meta property="og:title" content="SnakeTS" />
	<meta property="og:description" content="SnakeTS" />
	<meta property="og:url" content="https://snakets.netlify.app" />
</svelte:head>


<!-- App Shell -->
<AppShell>
	<svelte:fragment slot="header">
		<!-- App Bar -->
		<AppBar>
			<svelte:fragment slot="lead">
				<strong class="text-xl">SnakeTS</strong>
			</svelte:fragment>
			<svelte:fragment slot="trail">
				<a
					class="btn btn-sm variant-ghost-surface"
					href="https://instagram.com/abrahimzaman360"
					target="_blank"
					rel="noreferrer"
				>
					Instagram
				</a>
				<a
					class="btn btn-sm variant-ghost-surface"
					href="https://twitter.com/abrahimzaman360"
					target="_blank"
					rel="noreferrer"
				>
					X/Twitter
				</a>
				<a
					class="btn btn-sm variant-ghost-surface"
					href="https://github.com/abrahimzaman360"
					target="_blank"
					rel="noreferrer"
				>
					GitHub
				</a>
				<LightSwitch />
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<!-- Page Route Content -->
	<slot />
</AppShell>
