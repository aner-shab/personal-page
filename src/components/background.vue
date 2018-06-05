<template>
    <vue-particles
        color="#3e434a"
        :particleOpacity="1"
        :particlesNumber="80"
        shapeType="triangle"
        :particleSize="3"
        linesColor="#22283d"
        :linesWidth="6"
        :lineLinked="true"
        :lineOpacity="0.5"
        :linesDistance="150"
        :moveSpeed="1"
        :hoverEffect="true"
        hoverMode="grab"
        :clickEffect="false"
      >
      </vue-particles>
</template>

<script>
export default {
  name: 'Background',
  props: {
    numShapes: 3,
    maxSize: 20
  },
  methods: {
  },
  
  created: function(){
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

#particles-js {
  position: absolute;
  width: 99%;
  height: 99%;
  opacity: 0.9;
  z-index: -1;
  top: 0;
  left: 0;
}
</style>
