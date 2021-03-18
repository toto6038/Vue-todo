<template>
  <v-app>
    <!-- <v-app-bar
      app
      color="primary"
      dark
    >
    <v-btn text class="text-capitalize" text-lowecase exact :to="{name: 'Home'}">
      Home
    </v-btn>
    <v-btn text class="text-capitalize" text-lowecase exact :to="{name: 'About'}">
      About
    </v-btn>
    </v-app-bar> -->
    <navbar/>
    <v-main>
      <!-- <v-system-bar></v-system-bar> -->
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
// import HelloWorld from './components/HelloWorld'
import navbar from '@/components/Navbar'

export default {
  components: { navbar },
  name: 'App'
}
</script>
