<template>
  <v-navigation-drawer
    app
    fixed
    >
    <v-list shaped>
      <v-list-item two-line>
        <v-list-item-avatar>
          <img :src="require('../assets/logo.png')">
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title v-text="'SSA Group'"></v-list-item-title>
          <v-list-item-subtitle v-text="'Assessment'"></v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list-item-group class="mt-4" color="primary">
        <v-list-item class="mb-3" exact :to="{ name: 'Home' }">
          <v-list-item-icon>
            <v-icon v-text="'mdi-home'"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="'Home'"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item exact :to="{ name: 'About' }">
          <v-list-item-icon>
            <v-icon v-text="'mdi-note-outline'"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="'About'"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-navigation-drawer>
</template>
