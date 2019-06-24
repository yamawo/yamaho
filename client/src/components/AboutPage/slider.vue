<template>
  <div class="containar">
    <h1>{{ msg }}</h1>
    <slick ref="slick" :options="slickOptions">
	    <div><img src="../../assets/INTER-2.jpg"></div>
	    <div><img src="../../assets/griezmann-1.jpg"></div>
	    <div><img src="../../assets/yamasaki-1.png"></div>
    </slick>
  </div>
</template>

<script>
import Slick from 'vue-slick'
import '../../../node_modules/slick-carousel/slick/slick.css' 
export default {
	name: 'about',
	data () {
     return {
     	msg: 'This is "BIG3"',
     	slickOptions: {
     		arrows: false,
            autoplay: true,
            autoplaySpeed: 6000,
            dots: true,
            fade: true,
            appendDots: $('.dots')

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
    width: 100%;
}
</style>