<template>
  <v-toolbar color="grey">
		<v-app-bar-nav-icon></v-app-bar-nav-icon>

		<v-toolbar-title>Your Dashboard</v-toolbar-title>

		<v-spacer></v-spacer>

		<v-btn icon="mdi-magnify"></v-btn>

		<v-btn icon="mdi-dots-vertical"></v-btn>

		<template v-slot:extension>
			<v-tabs
				v-model="tab"
				align-tabs="center"
				bg-color="grey"
				stacked
			>
				<v-tab value="tab-1">
					<v-icon icon="mdi-phone"></v-icon>

					Recents
				</v-tab>

				<v-tab value="tab-2">
					<v-icon icon="mdi-heart"></v-icon>

					Favorites
				</v-tab>

				<v-tab value="tab-3">
					<v-icon icon="mdi-account-box"></v-icon>

					Nearby
				</v-tab>

				<v-tab value="tab-1">
					<v-icon icon="mdi-phone"></v-icon>

					Recents
				</v-tab>

				<v-tab value="tab-2">
					<v-icon icon="mdi-heart"></v-icon>

					Favorites
				</v-tab>

				<v-tab value="tab-3">
					<v-icon icon="mdi-account-box"></v-icon>

					Nearby
				</v-tab>

				<v-tab value="tab-1">
					<v-icon icon="mdi-phone"></v-icon>

					Recents
				</v-tab>

				<v-tab value="tab-2">
					<v-icon icon="mdi-heart"></v-icon>

					Favorites
				</v-tab>

				<v-tab value="tab-3">
					<v-icon icon="mdi-account-box"></v-icon>

					Nearby
				</v-tab>

				<v-tab value="tab-1">
					<v-icon icon="mdi-phone"></v-icon>

					Recents
				</v-tab>

				<v-tab value="tab-2">
					<v-icon icon="mdi-heart"></v-icon>

					Favorites
				</v-tab>

				<v-tab value="tab-3">
					<v-icon icon="mdi-account-box"></v-icon>

					Nearby
				</v-tab>

				<v-tab value="tab-1">
					<v-icon icon="mdi-phone"></v-icon>

					Recents
				</v-tab>

				<v-tab value="tab-2">
					<v-icon icon="mdi-heart"></v-icon>

					Favorites
				</v-tab>

				<v-tab value="tab-3">
					<v-icon icon="mdi-account-box"></v-icon>

					Nearby
				</v-tab>
			</v-tabs>
		</template>
	</v-toolbar>

</template>

<script>
export default {
  name: 'Navbar',
  methods: {
    toggleDrawer() {
      // Logic to toggle navigation drawer
    }
  }
}
</script>

<style scoped>
/* Add any custom styles here */
</style>
