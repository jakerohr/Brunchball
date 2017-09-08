<template>
  <nav class="navbar">
    <div class="navbar-brand">
      <nuxt-link to="/" class="navbar-item is-size-4">Brunchball</nuxt-link>
      <div v-on:click="toggleBurger" class="navbar-burger" v-bind:class="{ 'is-active': isActive }" data-target="navMenubd-example">
        <span></span>
        <span></span>
        <span></span>
      </div>

    </div>
    <!-- TODO: add method to add remove active class. Or remove active class altogether -->
    <div id="navMenubd-example" class="navbar-menu has-text-right" v-bind:class="{ 'is-active': isActive }">
      <div class="navbar-end">
        <nuxt-link to="/about" class="navbar-item is-hoverable">About</nuxt-link>
        <nuxt-link to="/players" class="navbar-item is-hoverable">Players</nuxt-link>
        <nuxt-link to="/games" class="navbar-item is-hoverable">Games</nuxt-link>
        <nuxt-link to="/settings" class="navbar-item is-hoverable">Settings</nuxt-link>
      </div>

      <!-- <div class="navbar-end"></div> -->
  </div>
</nav>

</template>

<script>
export default {
  data () {
    return {
      isActive: false
    }
  },
  methods: {
    toggleBurger: function () {
      this.isActive = this.isActive === false
      return this.isActive
    }
  }
}
</script>

<style>
/*	.bd-emoji {
	  margin-right: 0.5em;
	  margin-top: 2px;
  }*/
  .navbar {
    /*border-bottom: 1px solid hsl(0, 0%, 21%);*/
    position: fixed;
    top: 0;
    right: 0;
    left: 0;
    z-index: 1030;
    background-color: #fafafa;

  }
</style>
