<template>
　<div id="app">
  <button type="button" class="menu-icon" @click="toggle">
    <i class="material-icons">{{ iconText }}</i>
  </button>
   <div class="menu" v-show="isOpen">
    <ul class="menu-list">
      <li><router-link to="/">Home</router-link></li>
      <li><router-link to="/about">About</router-link></li>
      <li><router-link to="/contact">Contact</router-link></li>
    </ul>
   </div>
　</div>
       
   

</template>


<script>
    export default {
        name:"header",
    	data(){
    		return{
                isOpen: false,
    			iconText: 'menu'
    		}
    	},
        methods: {
    	toggle: function() {
      this.isOpen = !this.isOpen;
      this.iconText = this.isOpen ? 'close' : 'menu';
    }
  }
};
</script>

<style  scoped>


.menu-icon {
  background-color: transparent;
  border: none;
  cursor: pointer;
  outline: none;

}

.menu-list {
  list-style-type: none;
  text-align: left;
}
</style>
