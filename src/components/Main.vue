<template>
<v-app>
  <Nav/>
  <Hero/>
</v-app>
</template>

<script>
import Nav from './Nav'
import Hero from './Hero'
export default {
  data () {
    return {
      
    }
  },
  components: {
    'Nav': Nav,
    'Hero': Hero
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
h1 {
  color: #ECF0F1;
}
#nav {
  background-color: #34495E;
}

#nav-title {
  font-family: 'Alfa Slab One', cursive;
  font-size: 32px;
}
</style>




