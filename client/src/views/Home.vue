<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <terminal />
    <keireki />
  </div>
</template>

<script>
// @ is an alias to /src
import Terminal from '@/components/terminal.vue'
import Keireki from "@/components/topPage/keireki.vue"

export default {
  name: 'home',
  components: {
    Terminal,
    Keireki
  }
}
</script>
