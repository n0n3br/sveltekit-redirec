<script lang="ts">
	import { onMount } from 'svelte';
	import { goto } from '$app/navigation';
	export let path: string;
	onMount(() => {
		if (!path) {
			console.error('Path not set');
			return;
		}
		goto(path);
	});
</script>
