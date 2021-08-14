<template>
  <v-app>
    <!-- <v-navigation-drawer app> </v-navigation-drawer> -->

    <v-app-bar app>
      <!-- -->
      <v-toolbar-title>lottery app</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-menu open-on-hover offset-y>
        <template v-slot:activator="{ on, attrs }">
          <v-avatar>
            <img
              v-bind="attrs"
              v-on="on"
              src="https://cdn.vuetifyjs.com/images/john.jpg"
              alt="John"
            />
          </v-avatar>
        </template>

        <v-list>
          <v-list-item
            v-for="(item, index) in items"
            :key="index"
            link
            :to="{ name: item.link }"
          >
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item>

          <v-list-item link @click="logout">
            <v-list-item-title>Deconnexion</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>

    <!-- Sizes your content based upon application components -->
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>

    <v-footer app>
      <!-- -->
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        { title: 'profile', link: 'profile' },
        { title: 'Packs', link: 'pack' },
      ],

      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',
    }
  },
  methods: {
    logout() {},
  },
}
</script>
