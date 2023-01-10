# SvelteKit Redirect

A Svelte component to make the redirect from the template possible.

It can be usefull when using component composition and there's a need to redirect based on a slot prop (let:prop)

## Example

```svelte

// src/components/User.svelte

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

// src/login/+page.svelte
<h1>Login page</h1>

// src/+page.svelte
<script>
  import User from '../components/User.svelte'
  import Redirect from 'sveltekit-redirect'
</script>
<User let:authenticated>
	{#if !authenticated}
		<Redirect path="login" />
	{:else}
		<h1>Home</h1>
	{/if}
</User>
```
