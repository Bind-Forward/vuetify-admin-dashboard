<!-- This renders any components insidet the dashboard with the elements you expect -->
<template>
  <v-app
    id="dashboard-view"
    dark>
    <core-filter />

    <core-toolbar />

    <core-drawer />

    <v-content>
      <v-fade-transition mode="out-in">
        <router-view />
      </v-fade-transition>
    </v-content>

    <core-footer v-if="$route.meta.name !== 'Maps'" />

  </v-app>
</template>

<script>
//feel free to rename the title
export default {
  name: 'DashboardView',
  metaInfo () {
    return {
      title: 'Vuetify Admin Dashboard by ClintOxx'
    }
  }
}
</script>

<style>

</style>
