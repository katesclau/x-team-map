<h1>Settings</h1>

<script>
	export let segment;
</script>

<div class="submenu">
	<a
		class:selected={segment === "profile"}
		href="settings/profile"
	>Profile</a>

	<a
		class:selected={segment === "notifications"}
		href="settings/notifications"
	>Notifications</a>

</div>

<slot></slot>
