<script>
	import '../app.postcss';

	// Floating UI for Popups
	import { computePosition, autoUpdate, flip, shift, offset, arrow } from '@floating-ui/dom';
	import { AppShell, Drawer, getDrawerStore, storePopup } from '@skeletonlabs/skeleton';
	storePopup.set({ computePosition, autoUpdate, flip, shift, offset, arrow });
	import { setModeCurrent } from '@skeletonlabs/skeleton';
	import { onMount } from 'svelte';
	import { initializeStores } from '@skeletonlabs/skeleton';
	initializeStores();
	let drawerStore = getDrawerStore();
	function drawerOpen() {
		drawerStore.open({
			position: "right",
			bgDrawer: "bg-light-yellow",
			width: "w-2/3"
		});
	}
	onMount(() => {
		setModeCurrent(true)
	})
	import Navigation from '../lib/Navigation.svelte';
</script>

<svelte:head>
	<title>Tiệm nạp hộ "Người Nghiện"</title>
</svelte:head>
<AppShell slotSidebarRight="bg-light-yellow rounded hidden fixed right-0 xl:block w-0 xl:w-56 text-right m-2 drop-shadow-md">
    <div class="bg-gradient-to-br from-black/0 to-black/0 text-transparent box-decoration-clone translate-x-8 -translate-y-2 text-right xl:hidden w-full xl:fixed" >
        <button class="xl:hidden btn" on:click={drawerOpen}>
			<img src="/img/logo.png" width="400" alt="">
        </button>
    </div>

	<svelte:fragment slot="sidebarRight">
		<Navigation />
	</svelte:fragment>

</AppShell>
<Drawer >
	<Navigation />
</Drawer>

	<slot />

<style>
	:global(body) {
		background-color: #8FBDD3;
		background-image: url('/img/bg_web.jpg');
	}
</style>