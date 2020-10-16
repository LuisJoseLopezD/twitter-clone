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
			{icon: 'https://pbs.twimg.com/profile_images/1294731791832698881/2TcJzEeY_200x200.jpg', name: 'Romero José', user: '@romerojoseing', time: '3h', tweet: 'css nativo no morirá jamás jajaja'},
			{icon: 'https://pbs.twimg.com/profile_images/1273436986506989573/Oq58WVEp_400x400.jpg', name: 'Marco Alejandro', user: '@kada9001', time: '5h', tweet: 'Dogs are great.'},
			{icon: 'https://pbs.twimg.com/profile_images/1309223687086841856/m4D7wSLy_400x400.jpg', name: 'Luis José López D.', user: '@LuisJoseLopezD', time: '7h', tweet: 'Tailwind CSS + Vue js'},
			{icon: 'https://pbs.twimg.com/profile_images/1300859119633653760/WqLrPPNR_400x400.jpg', name: 'CATERINA VALENTINO', user: '@CATERINAV', time: '8h', tweet: 'El mejor día posible mi gente. Buenos días!'}

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
