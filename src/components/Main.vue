<template>
<v-app pa-0 ma-0>
  <Nav/>
  <Hero/>
  <About/>
  <Clients/>
  <Contact/>
</v-app>
</template>

<script>
import Nav from './Nav'
import Hero from './Hero'
import About from './About'
import Clients from './Clients'
import Contact from './Contact'

export default {
  data () {
    return {
      
    }
  },
  components: {
    'Nav': Nav,
    'Hero': Hero,
    'About': About,
    'Clients': Clients,
    'Contact': Contact
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

#about {
  background-color: #34495E;
}
</style>




