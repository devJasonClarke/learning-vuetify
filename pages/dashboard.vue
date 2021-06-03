<template>
  <div>
    <h1>Dashboard</h1>

    <v-container class="grey lighten-5">
      <v-row md4 justify="space-around">
        <v-col class="red">
          <v-card  outlined tile>
            One of two columns
          </v-card></v-col
        >
    <v-spacer></v-spacer>
        <v-col class="yellow" >
          <v-card  outlined tile>
            One of two columns
          </v-card></v-col
        >
      </v-row>
    </v-container>


  <v-container class="grey lighten-5">
    <v-row
     
      justify="space-between"
    >
      <v-col
       sm='11'
      md='1'
      >
        <v-card
          class="pa-2"
          outlined
          tile
        >
          One of two columns
        </v-card>
      </v-col>
      <v-col
       md='3'
        sm='1'
      >
        <v-card
          class="pa-2"
          outlined
          tile
        >
          One of two columns
        </v-card>
      </v-col>
    </v-row>
  </v-container>
  </div>
</template>

<script>
export default {
  data: () => ({
    justify: ["start", "center", "end", "space-around", "space-between"]
  })
};
</script>

<style lang="scss" scoped></style>
