<template>
	<nav class="level">
		<!-- Left side -->
		<div class="level-left">
			<div class="level-item">
				<p class="subtitle is-5">
					<strong>{{ count }}</strong> {{ resource }}s
				</p>
			</div>
			<div class="level-item">
				<div class="field has-addons">
					<p class="control">
						<input
							class="input"
							type="text"
							:placeholder="'find a ' + resource"
							v-model="searchQuery"
						>
					</p>
					<p class="control">
						<button class="button">
							Search
						</button>
					</p>
				</div>
			</div>
		</div>

		<!-- Right side -->
		<div class="level-right">
			<p class="level-item">
				<router-link
					:to="`/admin/${resource}s/new`"
					class="button is-success"
				>New {{ resource }}</router-link>
			</p>
		</div>
	</nav>
</template>


<script>
export default {
	props: {
		count: {
			type: Number,
			default: 0
		},
		resource: {
			type: String
		}
	},
	data() {
		return {
			searchQuery: ''
		}
	},
	watch: {
		searchQuery(value) {
			this.$emit('searchQueryChanged', value)
		}
	}
}
</script>


<style lang="scss" scoped>
</style>