<script>
	import User from '../components/User.svelte';
	import Redirect from '$lib/components/Redirect.svelte';
</script>

<User let:authenticated>
	{#if !authenticated}
		<Redirect path="login" />
	{:else}
		<h1>Home</h1>
	{/if}
</User>
