<template>
  <div class="navbar">
  <button id="home" v-on:click="onClick($event)" :class="{highlight:'home' == selected}" @click="selected = 'home'">Home</button>
  <button id="about" v-on:click="onClick($event)" :class="{highlight:'about' == selected}" @click="selected = 'about'">About</button>
  <button id="contact" v-on:click="onClick($event)" :class="{highlight:'contact' == selected}" @click="selected = 'contact'">Contact</button>
  </div>
</template>

<script>
export default {
  name: 'Navigation',
  data: function(){
    return{
    selected: "home"
    }
  },
  props: {
    },
  methods: {
    onClick: function (event) {
      this.$emit('clicked',event.target.id);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.navbar{
  font-family: 'Fira Sans', sans-serif;
  font-size: 30px;
  text-align: right;
  width:99%;
  position:absolute;
  top: 0;
  /* opacity: 0.5;/ */
}


button {
  font-size: 1em;
  background-color: transparent;
  cursor: pointer;
  border-width: 0em;
  padding: .5em;
  border-style: none;
  color: whitesmoke;
  margin-right: 30px;
  outline: none;
  transition: 0.25s ease-in-out;
}

.highlight{
  color: steelblue;
  transition: 0.25s ease-in-out;
}


@media (max-width: 1050px) {
  .navbar{
    font-size: 30px;
  }
  button{
    margin-right: 30px;
  }
}
@media (max-width: 800px) {
  .navbar{
    font-size: 25px;
  }
  button{
    margin-right: 20px;
  }
}
@media (max-width: 650px) {
  .navbar{
    font-size: 20px;
  }
  button{
    margin-right: 20px;
  }
}
@media (max-width: 350px) {
  .navbar{
    font-size: 20px;
  }
  button{
    margin-right: 20px;
  }
}

</style>
