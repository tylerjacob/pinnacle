<template>
<v-container pa-0 fluid>
  <canvas id="canvas"></canvas>
  <div id="mountains">
    <h1>Web development for people, by people</h1>
  </div>
</v-container>
</template>

<script>
export default {
  data () {
    return {
      dy: 0,
      circleArray: []
    }
  },
  methods: {
    Circle (x, y, dy){
      let canvas = document.getElementById('canvas')
      let ctx = canvas.getContext('2d')
      this.x = x
      this.y = y
      this.dy = dy
      this.draw = () => {
        ctx.beginPath()
        ctx.arc(this.x, this.y,this.dy, Math.PI * 2, false)
        ctx.strokeStyle = 'white'
        ctx.fill()
      }
    },
    animate(){
      let canvas = document.getElementById('canvas')
      let ctx = canvas.getContext('2d')
      requestAnimationFrame(this.animate)
      ctx.clearRect(0, 0, innerWidth,innerHeight)
      for(let i = 0; i < this.circleArray.length; i++){
        this.circleArray[i].draw()
        this.dy++
      }
      if(this.dy > 850){
        this.dy = 0
      }
      this.dy += 1.6
    }
  },
  mounted(){
    for(let i = 0; i < 450; i++){
      let x = Math.random() * 1600
      let y = Math.random() * 900
      let dy = .6
      this.circleArray.push(new this.Circle(x,y,dy))
  }
  this.animate()
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

#canvas {
  background-color: rgba(94, 133, 159, .49);
  position: absolute;
  width: 1600px!important;
  height: 800px;
}

#mountains {
  position: relative;
  height: 100vh;
  z-index: 1;
  background-image: url('../assets/MTNS.png');
  background-size: cover;
  background-position: bottom center;
}

#mountains h1 {
  padding-top: 120px;
  text-transform: uppercase;
  text-align: center;
}

#hero h1 {
  display: block;
  position: relative;
  font-style: bold;
}
/* x */
</style>




