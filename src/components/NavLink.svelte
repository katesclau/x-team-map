<script>
  export let segment;
  export let route;
</script>

<style>
  .selected {
		position: relative;
		display: inline-block;
	}

	.selected::after {
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 2px;
		background-color: rgb(255,62,0);
		display: block;
		bottom: -1px;
	}

	li {
		display: block;
		float: left;
	}

	a {
		text-decoration: none;
		padding: 1em 0.5em;
		display: block;
  }
</style>

<li>
  <a 
    class='{segment === undefined ? "selected" : ""}' 
    href={route.slug || ''}
  >{route.title}</a>
</li>