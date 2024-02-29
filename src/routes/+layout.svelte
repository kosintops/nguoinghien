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
    <div class="text-black text-right xl:hidden w-full" >
		<strong class="text-2xl float-left m-2">Tiệm nạp hộ "NGƯỜI NGHIỆN"</strong>
        <button class="xl:hidden btn btn-sm" on:click={drawerOpen}>
            <span>
                <svg viewBox="0 0 100 80" class="fill-token w-9 h-9">
                    <rect width="100" height="20" />
                    <rect y="30" width="100" height="20" />
                    <rect y="60" width="100" height="20" />
                </svg>
            </span>
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