<template>
  <div>
    <v-app-bar
  flat
  app
 shaped  dark class="green">
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Title</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar>
    <v-btn elevation="2" @click="change">{{ text }}</v-btn>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: "Please click me"
    };
  },
  methods: {
    change() {
      this.text = "thank you!";
    }
  }
};
</script>

<style lang="scss" scoped></style>
