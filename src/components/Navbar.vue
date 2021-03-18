<template>
    <nav>
        <v-toolbar color="blue">
            <v-app-bar-nav-icon @click.stop="drawer=!drawer"></v-app-bar-nav-icon>
            <v-toolbar-title class="text-uppercase">Todo list</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn  color="grey lighten-1" href="http://w1.csie.ntnu.edu.tw/members/bio.php?PID=42">
                neokent's office
                <v-icon right>mdi-exit-to-app</v-icon>
            </v-btn>
        </v-toolbar>
    <v-navigation-drawer v-model="drawer" temporary app color="blue darken-1">
    </v-navigation-drawer>
    </nav>
</template>

<script>
export default {
  data () {
    var drawer = false
    return {
      drawer
    }
  }
}
</script>
