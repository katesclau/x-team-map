<script>
	export let segment;
</script>

<style>
	nav {
		border-bottom: 1px solid rgba(255,62,0,0.1);
		font-weight: 300;
		padding: 0 1em;
	}

	ul {
		margin: 0;
		padding: 0;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}

</style>

<div>
	<nav>
		<ul>
			<slot></slot>
			<!--
			<li><a class='{segment === undefined ? "selected" : ""}' href='.'>home</a></li>
			<li><a class='{segment === "about" ? "selected" : ""}' href='about'>about</a></li>
			<li><a rel=prefetch class='{segment === "blog" ? "selected" : ""}' href='blog'>blog</a></li>
			<li><a rel=prefetch class='{segment === "settings" ? "selected" : ""}' href='settings'>settings</a></li>
			-->
		</ul>
	</nav>
</div>
