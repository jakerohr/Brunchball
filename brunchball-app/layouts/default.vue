<template>
  <div>
    <navbar/>
    <div class="body-main">
      <nuxt/>
    </div>
  </div>
</template>

<style>

</style>

<script>
import Navbar from '~/components/Navbar.vue'

export default {
  components: {
    Navbar
  }
}
</script>

<style>
  .body-main {
    margin-top: 64px;
  }
</style>