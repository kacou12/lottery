<template>
  <v-card :loading="loading" class="mx-auto my-12" max-width="374">
    <template slot="progress">
      <v-progress-linear
        color="deep-purple"
        height="10"
        indeterminate
      ></v-progress-linear>
    </template>

    <!-- <v-img height="250" :src="pack.image"></v-img> -->
    <v-img height="250" :src="pack.image"></v-img>

    <v-card-title>{{ pack.title }}</v-card-title>

    <v-card-text>
      <v-row align="center" class="mx-0">
        <v-rating
          :value="pack.rating"
          color="amber"
          dense
          half-increments
          readonly
          size="14"
        ></v-rating>

        <div class="grey--text ms-4">
          {{ pack.rating }} ({{ pack.participant }})
        </div>
      </v-row>

      <div class="my-4 text-subtitle-1">Mise: {{ pack.mise }} EUROS</div>
      <div class="my-4 text-subtitle-1">
        Gain Potentiel: {{ pack.gain }} EUROS
      </div>
      <div class="my-4 text-subtitle-2">Particpants: {{ pack.gain }}</div>

      <div>
        {{ pack.description }}
      </div>
    </v-card-text>

    <v-divider class="mx-4"></v-divider>
    <div>
      <div class="row align-center ml-1 my-5">
        <v-card-title>Horaire de lancement</v-card-title>
        <v-chip>{{ pack.horaire }}</v-chip>
      </div>
    </div>

    <v-card-actions class="d-flex justify-center">
      <v-btn color="deep-purple lighten-2 " @click="reserve">
        Participer
      </v-btn>
    </v-card-actions>
  </v-card>
</template>
<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: {
    pack: {
      type: Object,
      required: true,
    },
  },
  data: () => ({
    loading: false,
    selection: 1,
  }),

  methods: {
    reserve() {
      this.loading = true

      setTimeout(() => (this.loading = false), 2000)
    },
  },
})
</script>