<template>
  
  <aside class="sideMenu column is-2 is-narrow-mobile is-fullheight section is-hidden-mobile has-background-dark">
    <p class="menu-label is-hidden-touch has-text-white">Navigation</p>
    <ul class="menu-list">
      <li>
        <a href="/Home" :class="{ 'is-active': activeNum == 0 }" @click="changeActiveLink(0)">
          <span class="icon"><i class="fa fa-home"></i></span> Home
        </a>
      </li>
      <li>
        <a href="#" :class="{ 'is-active': activeNum == 1 }" @click="changeActiveLink(1)">
          <span class="icon"><i class="fa fa-book"></i></span> Other
        </a>
        <ul>
          <li>
            <a href="https://twitter.com/tamachan_zzz" target="blank" :class="{ 'is-active': activeNum == 10 }" @click="changeActiveLink(10)">
              <span class="icon is-small"><i class="fa fa-link"></i></span> Twitter
            </a>
          </li>
          <li>
            <a href="https://www.instagram.com/yamao_123/" target="blank" :class="{ 'is-active': activeNum == 11 }" @click="changeActiveLink(11)">
              <span class="icon is-small"><i class="fa fa-link"></i></span> Instagram
            </a>
          </li>
        </ul>
      </li>
      <li>
        <a href="/About" :class="{ 'is-active': activeNum == 13 }" @click="changeActiveLink(13)">
          <span class="icon"><i class="fa fa-info"></i></span> About
        </a>
      </li>
      <li>
        <a href="/Contact" :class="{ 'is-active': activeNum == 14 }" @click="changeActiveLink(14)">
          <span class="icon"><i class="fa fa-info"></i></span> Contact
        </a>
      </li>
    </ul>
  </aside>
</template>

<script>
export default {
  data () {
    return {
      activeNum: 0
    }
  },
  methods: {
    changeActiveLink (n) {
      this.activeNum = n
    }
  }
}
</script>
<style lang="css" scoped>
.sideMenu{
  z-index:999;
}
</style>
