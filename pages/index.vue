<template>
  <div>

    <h1>Yes bro</h1>
    <p class="red--text">
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Eaque totam
      dolore asperiores, ab enim, veniam libero vero dolorem cumque et odio
      ipsam assumenda sint animi qui dolorum aliquid ullam eveniet.
    </p>
    <p class="teal lighten-5 teal--text text--darken-5">
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Eaque totam
      dolore asperiores, ab enim, veniam libero vero dolorem cumque et odio
      ipsam assumenda sint animi qui dolorum aliquid ullam eveniet.
    </p>
    <h2 class="text-h1">Larke</h2>
    <v-btn depressed class="green darken-3 white--text">Your Face</v-btn>
    <v-btn color="pink lighten-4" dark depressed>
      <v-icon left color="red">
        mdi-login mdi-24px
      </v-icon>
      <span>Login</span>
    </v-btn>

    <v-btn fab outlined icon small color="red" depressed @click="like = !like">
      <v-icon v-if="like" small>
        mdi-heart
      </v-icon>

      <v-icon v-else small>
        mdi-heart-outline
      </v-icon>
    </v-btn>

    <v-tooltip color="red lighten-4 red--text" bottom>
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          v-bind="attrs"
          v-on="on"
          fab
          outlined
          icon
          small
          color="red"
          depressed
          @click="like = !like"
        >
          <v-icon v-if="like" small>
            mdi-heart
          </v-icon>

          <v-icon v-else small>
            mdi-heart-outline
          </v-icon>
        </v-btn>
      </template>
      <span>Favourite</span>
    </v-tooltip>

    <p class="d-flex d-sm-none">Extra smaill</p>

    <v-btn class="" color="">
      <v-icon color="red">mdi-heart</v-icon>
    </v-btn>

    <v-card class="" elevation="1" max-width="250">
      <v-img
        height="200"
        src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
      >
        <v-layout justify-end>
          <v-flex shrink>
            <v-btn outlined icon large color="red">
              <v-icon color="red">
                mdi-heart
              </v-icon>
            </v-btn>
          </v-flex>
        </v-layout>
      </v-img>

      <v-card-text>
        <p class="">
          Run with the gun
        </p>
        <div class="text--primary">
          pull up
        </div>
      </v-card-text>
      <v-card-actions>
        <v-btn text color="">
          connect
        </v-btn>
      </v-card-actions>
    </v-card>


    <!--  <v-card
    :loading="loading"
    class="mx-auto my-12"
    max-width="374"
 
  >
    <template slot="progress">
      <v-progress-linear
        color="deep-purple"
        height="10"
        indeterminate
      ></v-progress-linear>
    </template>

    <v-img
      height="250"
      src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
    ></v-img>

    <v-card-title>Cafe Badilico</v-card-title>

    <v-card-text>
      <v-row
        align="center"
        class="mx-0"
      >
        <v-rating
          :value="4.5"
          color="amber"
          dense
          half-increments
          readonly
          size="14"
        ></v-rating>

        <div class="grey--text ms-4">
          4.5 (413)
        </div>
      </v-row>

      <div class="my-4 subtitle-1">
        $ • Italian, Cafe
      </div>

      <div>Small plates, salads & sandwiches - an intimate setting with 12 indoor seats plus patio seating.</div>
    </v-card-text>

    <v-divider class="mx-4"></v-divider>

    <v-card-title>Tonight's availability</v-card-title>

    <v-card-text>
      <v-chip-group
        v-model="selection"
        active-class="deep-purple accent-4 white--text"
        column
      >
        <v-chip>5:30PM</v-chip>

        <v-chip>7:30PM</v-chip>

        <v-chip>8:00PM</v-chip>

        <v-chip>9:00PM</v-chip>
      </v-chip-group>
    </v-card-text>

    <v-card-actions>
      <v-btn
        color="deep-purple lighten-2"
        text
        @click="reserve"
      >
        Reserve
      </v-btn>
    </v-card-actions>
  </v-card>  -->
  </div>
</template>
<script>
export default {
  data: () => ({
    loading: false,
    selection: 1,
    like: false
  }),

  methods: {
    reserve() {
      this.loading = true;

      setTimeout(() => (this.loading = false), 2000);
    }
  }
};
</script>
