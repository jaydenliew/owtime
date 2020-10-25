<template>
  <section class="section_holder" id="popular_section">
		<div class="top_section">
			<h4>Popular on OWTIME</h4>
			<div class="link_holder">
				<a class="active" href="#">Featured</a>
				<a href="#">Award Winners</a>
				<a href="#">Trending</a>
			</div>
			<div class="indicator_holder">
				<button class="generic_btn" id="leftBtn" v-on:click="viewPoster('left')"></button>
				<button class="generic_btn" id="rightBtn" v-on:click="viewPoster('right')"></button>
			</div>
			<div class="poster_holder">
				<a id="pp1" href="#" class="generic_btn"></a>
				<a id="pp2" href="#" class="generic_btn"></a>
				<a id="pp3" href="#" class="generic_btn"></a>
				<a id="pp4" href="#" class="generic_btn"></a>
				<a id="pp5" href="#" class="generic_btn"></a>
				<a id="pp6" href="#" class="generic_btn"></a>
				<a id="pp7" href="#" class="generic_btn"></a>
				<a id="pp8" href="#" class="generic_btn"></a>
			</div>
		</div>
		<div class="btm_section">
			<div class="overlay"></div>
			<div class="description_content">
				<div class="title_content">
					<h1>Any Night Any Where, The Clever Way.</h1>
					<h3>The Ultimate Any Time Anywhere To Enjoy Your Time With The Movie.</h3>
				</div>
				<img src="../assets/images/Device@2x.png" />
			</div>
		</div>
	</section>
</template>

<script>
import $ from 'jquery'

var total = '';
var move = 50;

export default{
    methods:{
        viewPoster(data){
			switch(data){
				case 'left':
					total = parseInt(total+move);

					if(total > 0){
						total = 0;
						$('.poster_holder').stop().animate({left:total+'%'}, 500);
					}else{
						$('.poster_holder').stop().animate({left:total+'%'}, 500);
					}
					break;
				case 'right':
					total = parseInt(total-move);
					
					if(total < -115){
						total = -115;
						$('.poster_holder').stop().animate({left:total+'%'}, 500);
					}else{
						$('.poster_holder').stop().animate({left:total+'%'}, 500);
					}
					break;
			}
        }
    }
}
</script>