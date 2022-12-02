<template>
	<div id="app">
		
		<!-- feed -->
			<div v-for="user in users" v-bind:key="`${user.user}`" class="box container w-full p-2 text-sm md:text-base">

				<div class="text-special flex justify-start space-x-2 p-2">
					<img class="rounded-full" width="50px" :src="`${user.icon}`" alt="" />
					<h3 class="font-bold pl-1 cursor-pointer">{{user.name}} ·</h3>
					<p class="cursor-pointer">{{user.user}} ·</p>
					<p>{{user.time}}</p>
				</div>

				<div class="-mt-8 ml-6 pl-12">
					<p>{{user.tweet}}</p>
				</div>

				<div class="text-special icons flex justify-between ml-16 pr-16">
					<button class="reply py-1 px-2 rounded-full"><i class="cursor-pointer fas fa-reply"></i></button>
					<button class="retweet py-1 px-2 rounded-full"><i class="cursor-pointer fas fa-retweet"></i></button>
					<button class="heart py-1 px-2 rounded-full"><i class="cursor-pointer far fa-heart"></i></button>
					<button class="reply py-1 px-2 rounded-full"><i class="cursor-pointer far fa-chart-bar"></i></button>
				</div>
			
			</div>

	</div>
</template>

<script>

export default {
	
	name: 'App',

	data(){
		return {
		users: [ 
			{icon: 'https://media.istockphoto.com/id/1327592480/es/vector/icono-de-marcador-de-posici%C3%B3n-de-foto-de-avatar-predeterminado-foto-de-perfil-gris-hombre-de.jpg', name: 'Romero', user: '@romerojoseing', time: '3h', tweet: 'css nativo no morirá jamás jajaja'},
			{icon: 'https://media.istockphoto.com/id/1327592466/es/vector/icono-de-marcador-de-posici%C3%B3n-de-foto-de-avatar-predeterminado-foto-de-perfil-gris-hombre-de.jpg', name: 'Sando', user: '@kada9001', time: '5h', tweet: 'Dogs are great.'},
			{icon: 'https://media.istockphoto.com/id/1327592420/es/vector/icono-de-marcador-de-posici%C3%B3n-de-foto-de-avatar-predeterminado-foto-de-perfil-gris-hombre-de.jpg', name: 'Luis José', user: '@LuisJoseLopezD', time: '7h', tweet: 'Tailwind CSS + Vue js'}

				],
			}
		}

	}
</script>

<style scoped>

.box {
	border: 1px solid rgba(255, 255, 255, 0.2);
}

.box .icons .reply:hover {
	color: #1DA1F2;
}

.box .icons .retweet:hover {
	color: #17bf63;
}

.box .icons .heart:hover {
	color: #dd235e;
}

</style>
