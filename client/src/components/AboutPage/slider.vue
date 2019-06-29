<template>

  <div>
  <h1>{{ msg }}</h1>
  <b-carousel
    id="carousel-fade"
    style="text-shadow: 0px 0px 2px #000"
    fade
    indicators
    
  >
    <b-carousel-slide
      caption="First slide"
      src="~/assets/INTER-2.jpg"
    ></b-carousel-slide>
    <b-carousel-slide
      caption="Second Slide"
      img-src="../../assets/griezmann-1.jpg"
    ></b-carousel-slide>
    <b-carousel-slide
      caption="Third Slide"
      img-src="../../assets/yamasaki-1.png"
    ></b-carousel-slide>
  </b-carousel>
    <div class="profile">
        <ul>
            <li>氏名：山﨑　翔太,YAMASAKI SHOTA</li>
            <li>出身大学：大阪工業大学 工学部 環境工学科</li>
            <li>趣味：サッカー観戦,プログラミング</li>
        </ul>
    </div>
        <div class="university">
        </div>   
            <div class="giriezmann">
            </div>
                <div class="skill">
                </div>
</div>
 
  
</template>

<script>
import Slick from 'vue-slick'
import '../../../node_modules/slick-carousel/slick/slick.css' 
export default {
	name: 'slider',
	data () {
     return {
     	msg: 'This is "BIG3"',
     	slickOptions: {
     		    arrows: false,
            autoplay: true,
            autoplaySpeed: 5500,
            fade: true
     	}
     }
	},
	components: {
		Slick
	}
}
</script>

<style scoped>
slick {
    max-width: 300px;
    margin: 0;
    auto: 50px;
    padding: 0;
    height: auto;
}

img {
    height: 30vh;
    margin: 0 auto;
}
</style>