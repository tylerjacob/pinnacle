<template>
<v-container pa-0 fluid>
  <canvas id="canvas" ></canvas>
  <div id="mountains"></div>
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
        ctx.strokeStyle = 'yellow'
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
      }
      if(this.dy > 850){
        this.dy = 0
      }
      this.dy += 1.6
    }
  },
  mounted(){
    for(let i = 0; i < 45; i++){
      let x = Math.random() * window.innerWidth
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
  position:fixed;
  left:0;
  z-index: 1;
  background-color: rgba(94, 133, 159, .49);
  height: 98vh;
}

#mountains {
  position: relative;
  z-index: 2;
  margin-top: 23em;
  height: 60vh;
  background-image: url('MTNS.png');
}
</style>




