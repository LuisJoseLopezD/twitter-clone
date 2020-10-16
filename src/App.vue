<template>
	<div id="app" class="flex container h-screen w-full">
	
		<!-- side nav -->
		<div class="side-nav lg:w-1/5 py-2">
			<sidenav />
		</div>

		<!-- tweet component -->
		<div class="tweet w-full w-auto lg:w-1/2 py-2">
			<twittear />
			<tweet />
		</div>


		<!-- side nav RIGHT -->
		<div class="min-w-1/3 m-4 hidden lg:block">
			<sidenavright />
		</div>

	</div>
</template>

<script>

import tweet from './components/tweet.vue'
import sidenav from './components/sidenav.vue'
import twittear from './components/twittear.vue'
import sidenavright from './components/sidenavright.vue'

export default {
	
	name: 'App',

	components: {
		tweet,
		sidenav,
		twittear,
		sidenavright
	}

}

</script>

<style>

</style>
