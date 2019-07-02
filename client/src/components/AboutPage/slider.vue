<template>

  <div>
  <h1>{{ msg }}</h1>
  <b-carousel
    id="carousel-fade"
    style="text-shadow: 0px 0px 2px #000"
    fade
    indicators
    img-height="300"
  >
    <b-carousel-slide
      v-for="carousel in carouselList"
      :key="carousel.src"
      :caption="carousel.description"
      :img-src="carousel.src"
    > 
    </b-carousel-slide>
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
export default {
  name: 'slider',
  data () {
     return {
      msg: 'This is "BIG3"',
     }
  },
  computed:{
    carouselList:()=>{
      return [
        {src:"/img/about/INTER-2.jpg",description:"inter"},
        {src:"/img/about/griezmann-1.jpg",description:"griezman"},
        {src:"/img/about/yamasaki-1.png",description:"yamao"},
      ]
    }
  }
}
</script>

<style scoped>

img {
    height: 30vh;
    margin: 0 auto;
}
</style>