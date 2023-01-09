# SvelteKit Redirect

A Svelte component to make the redirect from the template possible

## Example

```svelte
// src/test/+page.svelte
<h1>Redirect test page</h1>

// src/+page.svelte
<script>
  import Redirect from '@n0n3br/sveltekit-redirect'
  export let redirect = true;
</script>
<h1>Main page</h1>
{#if redirect}
    <Redirect path="test">
{/if}
```
