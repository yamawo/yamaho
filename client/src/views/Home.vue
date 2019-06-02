<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <terminal />
  </div>
</template>

<script>
// @ is an alias to /src
import Terminal from '@/components/terminal.vue'
export default {
  name: 'home',
  components: {
    Terminal
  }
}
</script>
