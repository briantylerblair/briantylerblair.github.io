<template>
  <!-- Don't drop "q-app" class -->
  <div id="q-app">
    <app-header></app-header>
  </div>
</template>

<script>
import Header from './components/Header'
/*
 * Root component
 */
export default {
  components: {
    appHeader: Header
  }
}
</script>

<style></style>
