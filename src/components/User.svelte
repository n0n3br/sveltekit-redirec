<script lang="ts">
	let authenticated = false;

	interface $$Slots {
		default: { authenticated: boolean };
	}
</script>

<div>
	<h1>User component</h1>
	<slot {authenticated} />
</div>
