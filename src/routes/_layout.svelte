<script>
	import { onMount } from 'svelte';
  import Nav from '../components/Nav.svelte';
  import NavLink from '../components/NavLink.svelte';
	import routes from './routes.json';
	
	export let segment;

	onMount(async () => {
		segment = segment || { 
			title: 'Home',
			slug: '',
		};
	})
</script>

<style>
	main {
		position: relative;
		max-width: 56em;
		background-color: white;
		padding: 2em;
		margin: 0 auto;
		box-sizing: border-box;
	}
</style>

{@debug routes}
<Nav {segment}>
	{#each routes as route}
		{@debug route}
		<NavLink {segment} {route}/>
	{/each}
</Nav>

<main>
	<slot></slot>
</main>