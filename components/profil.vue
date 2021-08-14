<template>
  <v-card class="mx-auto" max-width="500">
    <v-img
      class="white--text align-end"
      height="200px"
      src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
    >
      <!-- <v-card-title>Top 10 Australian beaches</v-card-title> -->
    </v-img>

    <!-- <v-card-subtitle class="pb-0">John Doe</v-card-subtitle> -->

    <v-card-text class="text--primary">
      <div class="d-flex">
        <p>Mon solde :</p>
        <p>12559966</p>
      </div>
      <div class="d-flex">
        <p>Mon adresse:</p>
        <p>125sdbf4585df589dhbhld5454ds5ddbjhk774d7j45pi48888</p>
      </div>

      <!-- <div>Whitsunday Island, Whitsunday Islands</div> -->
    </v-card-text>

    <v-card-actions>
      <!-- <nuxt-link to="pack">Acheter</nuxt-link> -->
      <v-btn color="orange" text to="pack"> Acheter </v-btn>

      <!-- <v-btn color="orange" text> Explore </v-btn> -->
    </v-card-actions>
  </v-card>
</template>
