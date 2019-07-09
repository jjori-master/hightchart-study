<template>
	<v-navigation-drawer
		v-model="drawer"
		:mini-variant.sync="mini"
		hide-overlay
		stateless
	>
		<v-list class="pt-0" dense>
			<v-divider></v-divider>

			<v-list-tile v-for="item in items" :key="item.title">
				<v-list-tile-action>
					<v-icon>{{ item.icon }}</v-icon>
				</v-list-tile-action>

				<v-list-tile-content>
					<v-list-tile-title>{{ item.title }}</v-list-tile-title>
				</v-list-tile-content>
			</v-list-tile>
		</v-list>
	</v-navigation-drawer>
</template>

<script>
export default {
	data() {
		return {
			drawer: true,
			items: [
				{ title: 'Home', icon: 'fas fa-brain 2x' },
				{ title: 'About', icon: 'question_answer' },
			],
			mini: false,
			right: null,
		};
	},
};
</script>
