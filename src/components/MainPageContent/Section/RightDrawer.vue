<template>
  <v-app>
  <v-btn icon @click.stop="drawerRight = !drawerRight">
    <v-icon color="blue">mdi-apps</v-icon>
  </v-btn>
  <v-navigation-drawer
      v-model="drawerRight"
      app
      clipped
      right
      temporary
  >
    <v-list dense>
      <v-list-item @click.stop="right = !right">
        <v-list-item-action>
          <v-icon>mdi-exit-to-app</v-icon>
        </v-list-item-action>
        <v-list-item-content>
          <v-list-item-title>Open Temporary Drawer</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
  <v-navigation-drawer
      v-model="right"
      fixed
      right
      temporary
  ></v-navigation-drawer>
  </v-app>
</template>

<script>
export default {
name: "RightDrawer",
  props: {
    source: String,
  },
  data: () => ({
    drawer: false,
    drawerRight: false,
    right: false,
    left: false
  }),
}
</script>

<style scoped>

</style>