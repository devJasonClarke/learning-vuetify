<template>
  <v-app>
    <nav>
      <v-toolbar flat>
        <v-app-bar-nav-icon
          class="d-md-none  ml-sm-4 ml-xs-1"
          @click.stop="drawer = !drawer"
        ></v-app-bar-nav-icon>
        <h1 class="ml-md-7 ml-sm-3 text-h5 font-weight-bold">Nav Bar</h1>
        <v-spacer></v-spacer>

        <div class="d-none d-sm-flex">
          <v-btn text :to="{ name: 'test' }">Test</v-btn>
          <v-btn text :to="{ name: 'dashboard' }">Dashboard</v-btn>
          <v-btn text>Link</v-btn>
          <v-btn text>Link</v-btn>
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
          
            <v-list-item-title >Foo </v-list-item-title>
        
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Bar</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Fizz</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Buzz</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <v-container>
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
</style>
