<template>

	<div>
		<div class="navbar-brand">
			<a href="/">
				<img src="https://bulma.io/images/bulma-logo.png">
			</a>
		</div>

		<nav class="is-hidden-mobile">
			<h5 class="heading">ADMIN</h5>

			<router-link to="/admin/">Dashboard</router-link>

			<h5 class="heading">RESOURCES</h5>

			<router-link to="/admin/posts">Posts</router-link>
			<router-link to="/admin/comments">Comments</router-link>
			<router-link to="/admin/users">Users</router-link>

			<h5 class="heading">GENERAL</h5>

			<a href="/">Homepage</a>
			<a href="/logout">Logout</a>
		</nav>
	</div>

</template>


<script>
export default {}
</script>


<style lang="scss" scoped>
.heading {
	margin-top: 4em;
}
</style>