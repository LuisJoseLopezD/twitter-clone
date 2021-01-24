<!-- <h3 class="text-twittear pl-1 font-semibold text-base md:text-lg">¿Qué está pasando?</h3> -->

<template>
	<div id="app">
		
		<!-- twittear -->

			<div class="container w-full flex justify-between px-4 py-2 text-special">
				<p class="font-bold text-lg">Inicio</p>
				<i class="cursor-pointer fas fa-reply"></i>
			</div>

			<div class="box container w-full p-2">

				  <div class="flex justify-start space-x-2 place-items-center">
				    <img class="rounded-full" width="50px" src="https://avatars.githubusercontent.com/u/45377927?s=460&u=028d0c62c9134662a2fb51c04f5cdc6ee025ffc7&v=4" alt="" />
				    <input class="search w-full outline-none rounded-full p-2 text-white px-2 placeholder-white font-semibold text-base md:text-lg focus:placeholder-opacity-0" type="text" name="search" placeholder="¿Qué está pasando?" autcomplete="off" />
				  </div>

				<div class="icons flex justify-between place-items-center space-x-6 ml-16 py-1">
					<div class="buttons-twittear space-x-4 sm:space-x-6 sm:text-sm md:text-xl">
						<i class="cursor-pointer fas fa-image"></i>
						<i class="cursor-pointer fas fa-smile"></i>
						<i class="cursor-pointer far fa-chart-bar"></i>
						<i class="cursor-pointer far fa-calendar"></i>
					</div>
					<div>
						<button class="button-twittear mr-2 text-white text-sm-center px-2 py-1 md:px-4 md:py-2 rounded-full bg-blue font-bold">Twittear</button>
					</div>
				</div>
			
			</div>

	</div>
</template>

<script>

export default {
	
	name: 'App'

	}
</script>

<style scoped>

.box {
	border: 1px solid rgba(255, 255, 255, 0.2);
}

.box .text-twittear {
	color: #6e767d;
} 

.box .icons .buttons-twittear{
	color: #1DA1F2;
}

.box .search {
	background: #14171a;
}

</style>
