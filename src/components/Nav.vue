<template>
  <v-toolbar fixed id='nav'>
    <v-toolbar-title id='nav-title' class="white--text">Pinnacle</v-toolbar-title>
    <v-spacer></v-spacer>
    <v-btn icon>
      <v-icon>home</v-icon>
    </v-btn>
    <v-btn icon>
      <v-icon>people</v-icon>
    </v-btn>
    <v-btn icon>
      <v-icon>mail</v-icon>
    </v-btn>
    
  </v-toolbar>
</template>

<script>
export default {
  data () {
    return {
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
h1 {
  color: white;
}
#nav {
  background-color: #34495E;
}

#nav-title {
  font-family: 'Alfa Slab One', cursive;
  font-size: 32px;
}
</style>




