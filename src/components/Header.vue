<template>
  <q-layout>
    <div slot="header" class="toolbar">

      <button class="hide-on-drawer-visible" @click="$refs.drawer.open()">
        <i>menu</i>
      </button>
      <q-toolbar-title :padding="1">
        Brian Tyler Blair
      </q-toolbar-title>
    </div>
    <q-drawer ref="drawer">
      <div class="list no-border platform-delimiter">
        <img class="shadow-2 drawer-logo" src="../assets/p-logo.png">
        <hr />
        <q-drawer-link icon="mail" :to="{path: '/', exact: true}">
          Home
        </q-drawer-link>
        <q-drawer-link icon="view_quilt" :to="{path: '/projects', exact: true}">
          Projects
        </q-drawer-link>
        <q-drawer-link icon="account_circle" :to="{path: '/about', exact: true}">
          About Me
        </q-drawer-link>
      </div>
    </q-drawer>

    <router-view class="layout-view"></router-view>

  </q-layout>
</template>

<script>
export default {
  data () {
    return {}
  }
}
</script>

<style lang="styl" scoped>
.drawer-logo {
  display block
  width 200px
  height 200px
  margin auto
  border-radius 50%
}
</style>
