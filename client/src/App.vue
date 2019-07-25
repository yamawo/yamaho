<template>
  <div id="containar">
    <div class="main-content columns is-fullheight">
      <SideMenu  />
      <div class="container column is-10">
       <router-view /> 
      </div>
    </div>
  </div>
</template>


<script>
import SideMenu from '@/components/topPage/SideMenu'


export default{
  name:"app",
  components:{
   SideMenu
  }

}

</script>


<style lang="sass">
// サイドメニューの色
$menu-item-active-background-color: hsl(171, 100%, 41%);
$menu-item-color: hsl(0, 0%, 100%);


@import '~bulma';
$fa-font-path: '~font-awesome/fonts/';
@import '~font-awesome/scss/font-awesome';

</style>
