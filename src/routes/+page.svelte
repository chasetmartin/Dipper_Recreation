<script>
	import { slide } from "svelte/transition";
	import { fade } from "svelte/transition";
	import { blur } from "svelte/transition";
	import { onMount } from "svelte";
	import Seo from "$lib/components/seo.svelte";

	let showContent = false; // Variable to control the initial visibility of the content

	// After the component is rendered, set showContent to true to trigger the transitions
	onMount(() => {
		showContent = true;
	});
</script>
<Seo 
title="Dipper.pro" 
description="A new recreation hub built for those who dive into adventure. Recreation data, community forums, and more!" 
keywords="river, flow, forecast, community, whitewater, kayaking, rafting, canoeing, paddleboarding, SUP, forum, guage, hydrograph, camping, hiking, backpacking, campsites, overlanding"
type="website"
canonical="https://dipper.pro" 
/>

{#if showContent}
	<div in:slide={{duration:3000}}>
	<div in:fade={{duration:1500}} class="container w-full text-center mx-auto flex-auto p-8">
		<h1 class="h1 text-center p-3 customfont">DIPPER.pro</h1>
		<h2 class="h2 text-center p-2">a new recreation hub</h2>
		<h3 class="h3 text-center p-1">built for those who dive into adventure</h3>
	</div>
	<div in:fade={{duration:1500}} class="w-full grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-8 p-4">
		<a class="card card-hover overflow-hidden" href="https://river.dipper.pro">
			<header>
				<img src="NameLogoDarkSmall.svg" class="w-full aspect-[20/9] p-4 customfilter2" alt="River Dipper" />
			</header>
			<div class="p-4 space-y-4">
				<h2 class="h2 text-center">The next generation of river recreation community and resources!</h2>
			</div>
			<footer class="w-full text-center p-2 card-footer">
				river.dipper.pro
			</footer>
		</a>
		<div class="card overflow-hidden customfilter4">
			<header>
				<img src="CampDipper.svg" class="w-full aspect-[20/9] p-4 customfilter" alt="Camp Dipper" />
			</header>
			<div class="p-4 space-y-4 customfilter3">
				<h1 class="h1 text-center">Coming Soon!</h1>
				<article>
					<h3 class="h3 text-center pb-4">
						Community and collaboration on all things camping, backpacking, and overlanding!
					</h3>
				</article>
			</div>
		</div>
	</div>
	<div in:fade={{duration:1500}} class="container w-full text-center mx-auto flex-auto p-8 mt-4">
		<h4 class="h4 text-center">We're a small team working to build new, exciting communities in the outdoor recreation world</h4>
	</div>
</div>
{/if}

<style>
	.customfilter {
		filter: opacity(0.4);
	}
	.customfilter2 {
		filter: drop-shadow(0 0 0.25rem #000000);
	}
	.customfilter3 {
		filter: opacity(0.6);
	}

	.customfilter4 {
		filter: grayscale(50%);
	}
	.customfont {
		font-family: 'IndieFlower';
		font-size: 5em;
	}
</style>
