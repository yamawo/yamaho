<template>
<div id="app" >
  <header id="header">
<mobile-nav>
    <hamburger
        :stroke='2'
        :gap='5'
        color='#192a35'
        :open.sync='open'>
    </hamburger>
</mobile-nav>
  </header>
</div>
</template>

<script>
import 'vue-hamburger/index.css'
Vue.component('hamburger', require('vue-hamburger'))
 

export default{
        name: 'headermenu',


components:('mobile-nav',{
  data: function() {
    return {
      open: false 

    }
  }
})}
</script>

<style scoped>
</style>


<ul class="menu-list">
      <li><router-link to="/">Home</router-link></li>
      <li><router-link to="/about">About</router-link></li>
      <li><router-link to="/contact">Contact</router-link></li>
    </ul>