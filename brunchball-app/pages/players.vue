<template>
  <section class="container">
    <div class="columns is-multiline is-centered">
      <div class="column is-8">
        <h1 class="is-size-1">
          Players
        </h1>
        <h2 class="is-size-2">
          Add some players here
        </h2>
        <player-form/>
      </div>
    </div>
  </section>
</template>

<script>
import PlayerForm from '~/components/PlayerForm.vue'

export default {
  components: {
    PlayerForm
  }
}
</script>

<style>


</style>
