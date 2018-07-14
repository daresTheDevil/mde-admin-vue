<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      clipped
      fixed
      app
    >
      <v-list dense>
        <v-list-tile>
          <v-list-tile-action>
            <v-icon>dashboard</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Dashboard</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-list-tile>
          <v-list-tile-action>
            <v-icon>settings</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Settings</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    
    <v-toolbar app fixed clipped-left>
      <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title>
        <router-link to="/" tag="span" style="cursor: pointer">
          {{ appTitle }}
        </router-link>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn v-for="item in menuItems"
          :key="item.title"
          :to="item.path"
        >
        <v-icon left dark>{{ item.icon }}</v-icon>
        {{ item.title }}
        </v-btn>
    </v-toolbar-items>
    </v-toolbar>
    
    <v-content>
      <router-view></router-view>
    </v-content>
    
    <v-footer app fixed color="grey darken-3" height="auto">
      <v-container class="py-0 my-0" fluid>
        <v-layout row>
          <v-flex>
            <v-btn
              class="white--text title"
              flat
            >
              MSIS
              <v-icon right medium color="red lighten-2">web</v-icon>
              <v-icon right medium color="yellow lighten-2">network_check</v-icon>
              <v-icon right medium color="teal lighten-2">storage</v-icon>
            </v-btn>
          </v-flex>
          <v-flex>
            <v-btn
              class="white--text title"
              flat
            >
              TIMS
              <v-icon right medium color="red lighten-2">web</v-icon>
              <v-icon right medium color="yellow lighten-2">network_check</v-icon>
              <v-icon right medium color="teal lighten-2">storage</v-icon>
            </v-btn>
          </v-flex>
          <v-flex>
            <v-btn
              class="white--text title"
              flat
            >
              ELMS
              <v-icon right medium color="red lighten-2">web</v-icon>
              <v-icon right medium color="yellow lighten-2">network_check</v-icon>
              <v-icon right medium color="teal lighten-2">storage</v-icon>
            </v-btn>
          </v-flex>
          <v-flex>
            <v-btn
              class="white--text title"
              flat
            >
              WEB
              <v-icon right medium color="red lighten-2">web</v-icon>
              <v-icon right medium color="yellow lighten-2">network_check</v-icon>
              <v-icon right medium color="teal lighten-2">storage</v-icon>
            </v-btn>
          </v-flex>
          <v-flex>
            <v-btn
              class="white--text title"
              flat
            >
              MSRC
              <v-icon right medium color="red lighten-2">web</v-icon>
              <v-icon right medium color="yellow lighten-2">network_check</v-icon>
              <v-icon right medium color="teal lighten-2">storage</v-icon>
            </v-btn>
          </v-flex>
        </v-layout>
      </v-container>
    </v-footer>
  </v-app>
</template>

<script>
  export default {
    data() {
      return {
        appTitle: 'MSRC',
        menuItems: [
          { title: 'Home', path: '/home', icon: 'home' },
          { title: 'Sign Up', path: '/signup', icon: 'face' },
          { title: 'Sign In', path: '/signin', icon: 'lock_open' },
        ],
        drawer: true,
      };
    },
  };
</script>

<style>
  @import url('https://fonts.googleapis.com/css?family=Roboto:300,400,500,700|Material+Icons');
  /* Global CSS */
</style>
