<template>
	<div id="app">
		
		<!-- side nav RIGHT hidden lg:block -->

    <div class="relative">

      <span class="absolute inset-y-0 ml-2 mt-2"><i class="fas fa-search text-special"></i></span>

      <input class="search w-full outline-none bg-gray-600 rounded-full p-2 text-white focus:placeholder-opacity-0 px-8 placeholder-white" type="text" name="search" placeholder="Buscar en Twitter" autcomplete="off" />
    
    </div>

  <div class="trends-box bg-gray-600 rounded-md mt-2">
    
    <div class="flex justify-between place-items-center">
      <h3 class="trends-title text-white font-bold text-xl px-4 py-2 text-special">Tendencias para ti</h3>
      <button class="button-arrow rounded-full p-1 px-2 mr-4"><i class="fas text-blue fa-cog"></i></button>
    </div>

    <div v-for="trend in trends" v-bind:key="`${trend.hashtag}`" class="flex justify-between border-t border-b text-special">

      <div class="p-2 ml-2 text-special">
        <p class="text-gray-400 text-sm">{{trend.country}}</p>
        <p class="trend-column text-white font-bold text-special">{{trend.hashtag}}</p>
        <p class="text-gray-400 text-sm">{{trend.tweets}}</p>
      </div>

      <div class="mr-4 mt-1">
        <button class="button-arrow rounded-full p-1 px-2"><i class="fas text-sm fa-chevron-down"></i></button>
      </div>

    </div>  

    <div>
      <p class="show-more text-white text-base text-xl1 p-3 ml-2 cursor-pointer">Mostrar Más</p>
    </div>

  </div> 



	</div>
</template>

<script>

export default {
	
	name: 'App',

	data(){
		return {
		trends: [ 
			{country: 'Tendencia en Venezuela', hashtag: '#SinLuz', tweets:'3.727 Tweets'},
			{country: 'Tendencia en Venezuela', hashtag: '#SinLuz', tweets:'3.727 Tweets'},
			{country: 'Tendencia en Venezuela', hashtag: '#SinLuz', tweets:'3.727 Tweets'},
			{country: 'Tendencia en Venezuela', hashtag: '#SinLuz', tweets:'3.727 Tweets'},

				],
			}
		}

}

</script>

<style scoped>

.search, .trends-box {
	background-color: RGB(170,184,194,0.1);
}

.trends-box .show-more {
	color: #2795D9;
}

.trends-box .button-arrow:hover {
  color: #1DA1F2;
}

</style>
