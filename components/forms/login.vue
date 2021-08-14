<template>
  <v-form ref="form" v-model="valid" lazy-validation>
    <v-text-field
      v-model="adress"
      :counter="5"
      :rules="nameRules"
      label="Votre adresse"
      required
    ></v-text-field>

    <v-btn :disabled="!valid" color="success" class="mr-4" @click="validate">
      Validate
    </v-btn>

    <v-btn color="error" class="mr-4" @click="reset"> Reset Form </v-btn>
  </v-form>
</template>
<script>
export default {
  data: () => ({
    valid: true,
    adress: '',
    nameRules: [
      (v) => !!v || 'Adress is required',
      (v) => (v && v.length >= 5) || 'Adress must be more than 5 characters',
    ],
  }),

  methods: {
    validate() {
      this.$refs.form.validate()
    },
    reset() {
      this.$refs.form.reset()
    },
    resetValidation() {
      this.$refs.form.resetValidation()
    },
  },
}
</script>