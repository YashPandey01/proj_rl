<template>
  <v-app id="inspire">

    <!--NavigationRight-->
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
    <!--End of NavigationRight-->


    <!--AppBar-->
    <v-app-bar
        app
        clipped-right
        color="dark-grey"
        dark
        flat
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title >Affitto.</v-toolbar-title>
      <v-spacer></v-spacer>
      <SearchBottomNav/>
      <v-btn icon @click.stop="drawerRight = !drawerRight">
        <v-icon color="blue">mdi-apps</v-icon>
      </v-btn>
    </v-app-bar>
    <!--End of AppBar-->


    <!--NavigationLeft-->
    <v-navigation-drawer
        v-model="drawer"
        app
        mini-variant
        temporary
    >
      <v-list dense>
        <v-list-item @click.stop="left = !left">
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
        v-model="left"
        fixed
        temporary
    ></v-navigation-drawer>
    <router-view />
    <v-main>
      <v-container
          class="fill-height"
          fluid
      >
        <v-row
            justify="center"
            align="center"
        >
        </v-row>
      </v-container>
    </v-main>

    <v-navigation-drawer
        v-model="right"
        fixed
        right
        temporary
    ></v-navigation-drawer>
    <!--End of NavigationLeft-->

    <!--Footer-->
    <v-footer
        dark
        padless
    >
      <v-card
          flat
          tile
          class="black lighten-1 white--text text-center"
      >
        <v-card-text>
          <v-btn
              v-for="icon in icons"
              :key="icon"
              class="mx-4 white--text"
              icon
          >
            <v-icon size="24px">
              {{ icon }}
            </v-icon>
          </v-btn>
        </v-card-text>

        <v-card-text class="white--text pt-0">
          Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet. Mauris cursus commodo interdum. Praesent ut risus eget metus luctus accumsan id ultrices nunc. Sed at orci sed massa consectetur dignissim a sit amet dui. Duis commodo vitae velit et faucibus. Morbi vehicula lacinia malesuada. Nulla placerat augue vel ipsum ultrices, cursus iaculis dui sollicitudin. Vestibulum eu ipsum vel diam elementum tempor vel ut orci. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
        </v-card-text>

        <v-divider></v-divider>

        <v-card-text class="white--text">
          {{ new Date().getFullYear() }} — <strong>Affitto</strong>
        </v-card-text>
      </v-card>
    </v-footer>
    <v-footer
        app
        color="black"
        class="white--text"
    >
      <span>Affitto.com</span>
      <v-spacer></v-spacer>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
    <!--End of Footer-->

  </v-app>
</template>

<script>
import SearchBottomNav from "@/components/MainPageContent/Section/SearchBottomNav";
export default {
  name: "MainLayout",
  components:{
    SearchBottomNav
  },
  props: {
    source: String,
  },
  data: () => ({
    drawer: false,
    drawerRight: false,
    right: false,
    left: false,
    icons: [
      'mdi-facebook',
      'mdi-twitter',
      'mdi-linkedin',
      'mdi-instagram',
    ],
  }),

}
</script>