<template>
<div id="app" >
  <video src="/video/PexelsVideos.mp4" poster="/public/img/home/pexelPhoto.jpeg" autoplay loop preload="auto">
  </video>
</div>
</template>

<script>
export default {
  name: 'headermenu',
  components: {
      

      
  }
}
</script>

<style scoped>
video {
  position: fixed;
  right: 0;
  bottom: 0;
  min-width: 100%;
  min-height: 100%;
  width: auto;
  height: auto;
  z-index: 1;
}
</style>


<ul class="menu-list">
      <li><router-link to="/">Home</router-link></li>
      <li><router-link to="/about">About</router-link></li>
      <li><router-link to="/contact">Contact</router-link></li>
    </ul>