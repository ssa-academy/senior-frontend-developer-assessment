<template>
  <v-app>
    <Appbar />
    <Sidebar />

    <v-main>
      <v-container>
        <router-view></router-view>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Appbar from '@/components/Appbar.vue'
import Sidebar from '@/components/Sidebar.vue'

export default {
  name: 'App',

  components: {
    Appbar,
    Sidebar
  },

  data: () => ({
    //
  })
}
</script>
