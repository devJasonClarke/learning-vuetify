<template>
  <v-app>
    <nav>
      <v-toolbar flat>
        <v-app-bar-nav-icon
          class="d-md-none  ml-sm-4 ml-xs-1"
          @click.stop="drawer = !drawer"
        ></v-app-bar-nav-icon>
      <nuxt-link to="/">  <h1 class="ml-md-7 ml-sm-3 text-h5 font-weight-bold">Nav Bar</h1></nuxt-link>
        <v-spacer></v-spacer>

        <div class="d-none d-sm-flex">
          <v-btn text :to="{ name: 'test' }">Test</v-btn>
          <v-btn text :to="{ name: 'inspire' }">Inspire</v-btn>
          <v-btn text :to="{ name: 'dashboard' }">Dashboard</v-btn>
          <v-btn text :to="{ name: 'toolbar' }">Toolbar</v-btn>
          <v-btn color="blue" class=" darken-4 mr-4" depressed dark
            >Sign Up</v-btn
          >
        </div>
      </v-toolbar>
      <v-divider></v-divider>
    </nav>
    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list nav dense>
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
        >
          <v-list-item link to="/">
          
            <v-list-item-title >Home </v-list-item-title>
        
          </v-list-item>
          <v-list-item link :to="{name: 'test'}">
          
            <v-list-item-title >Test </v-list-item-title>
        
          </v-list-item>

          <v-list-item  link :to="{name: 'inspire'}">
            <v-list-item-title>Inspire</v-list-item-title>
          </v-list-item>

          <v-list-item  link :to="{name: 'dashboard'}">
            <v-list-item-title>Dashboard</v-list-item-title>
          </v-list-item>

          <v-list-item  link :to="{name: 'toolbar'}">
            <v-list-item-title>Toolbar</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <v-container fluid class="ma-0 pa-0">
        <nuxt />
      </v-container>
    </v-main>

  </v-app>
</template>

<script>
export default {
  data: () => ({
    drawer: false,
    group: null
  }),

  watch: {
    group() {
      this.drawer = false;
    }
  }
};
</script>
<style scoped>
.test {
  border-bottom: 3px solid red;
}
a{
  color: black;
text-decoration: none;
}
</style>
