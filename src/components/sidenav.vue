<template>
	<div id="app">
		
		<!-- side nav -->
			
			<button class="h-12 w-12 rounded-full text-2xl text-blue">
				<i class="fab fa-twitter"></i>
			</button>
			
			<div>
				<button v-for="tab in tabs" v-bind:key="`${tab.id}`" class="hover:text-blue text-xl flex p-2 rounded-full lg:mr-2 mb-2 text-special">
					<i :class="`${tab.icon} ml-1 text-2xl lg:mr-2 lg:text-left`"></i>
					<p class="text-lg lg:px-2 font-semibold text-left hidden lg:block"> {{tab.title}} </p>
				</button>
			</div>

			<!-- large button -->
			<button class="button-twittear text-white text-sm-center px-12 py-2 rounded-full bg-blue font-bold hidden lg:block">Twittear</button>

			<!-- small button -->
			<button class="button-twittear text-white ml-2 text-sm p-1 rounded-full bg-blue font-bold lg:hidden">TW</button>

	</div>
</template>

<script>

export default {
	
	name: 'App',

	data(){
		return {
		tabs: [ 
			{icon: 'fas fa-home', title: 'Inicio', id:'inicio'},
			{icon: 'fas fa-hashtag', title: 'Explorar', id:'explore'},
			{icon: 'fas fa-bell', title: 'Notificaciones', id:'notificaciones'},
			{icon: 'fas fa-envelope', title: 'Mensajes', id:'mensajes'},
			{icon: 'fas fa-user', title: 'Perfil', id:'perfil'},
			{icon: 'fas fa-ellipsis-h', title: 'Opciones', id:'opciones'}
				],
			}
		}
	}
</script>

<style>

body {
	background-color: RGB(20,23,26);
	color: white;
}

button:hover {
  background-color: RGB(170,184,194,0.1);
}

.button-twittear:hover {
	background-color: #2795D9;
}

.tweet, .side-nav {
	border-right: 1px solid rgba(255, 255, 255, 0.2);
}

</style>
