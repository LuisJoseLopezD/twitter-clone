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
			{icon: 'https://media-exp1.licdn.com/dms/image/C4E03AQFY8AZUxs1zyg/profile-displayphoto-shrink_200_200/0/1651957435009?e=1675296000&v=beta&t=qenl_s7S4O6R_R3TJ9WCogfEb81SVbtWPJzA4HUMRxw', name: 'Romero', user: '@romerojoseing', time: '3h', tweet: 'css nativo no morirá jamás jajaja'},
			{icon: 'https://media-exp1.licdn.com/dms/image/D4E03AQF4byDgJ5OUyQ/profile-displayphoto-shrink_200_200/0/1666996485914?e=1675296000&v=beta&t=joK6kajsRTYRM8z7JwjH0QzJlquj9oVV1Q0f4sNwovA', name: 'Sando', user: '@kada9001', time: '5h', tweet: 'Dogs are great.'},
			{icon: 'https://media-exp1.licdn.com/dms/image/D4E03AQGj8ScqatZnpg/profile-displayphoto-shrink_800_800/0/1668912775154?e=1675296000&v=beta&t=TzfFBavZz6Vnfj101Ci2iS_mNChufRrUvvJ30KJxWFM', name: 'Luis José', user: '@LuisJoseLopezD', time: '7h', tweet: 'Tailwind CSS + Vue js'}

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
