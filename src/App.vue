<template>
  <div id="app">
    <Background />
    <Navigation @clicked="onButtonClicked($event)"/>
    <transition
    name="custom-classes-transition"
    enter-active-class="animated slideInLeft"
    leave-active-class="animated bounceOutRight"
  >
    <Home v-if="this.selectedView == 'home'"/>
    <About v-if="this.selectedView == 'about'"/>
    <Contact v-if="this.selectedView == 'contact'"/>
    </transition> 
  </div>
</template>

<script>
import Home from './components/home.vue'
import About from './components/about.vue'
import Background from './components/background.vue'
import Navigation from './components/navigation.vue'
import Contact from './components/contact.vue'

export default {
  name: 'app',
  components: {
    Navigation,
    Background,
    Home,
    About,
    Contact
  },
  data:function() {
    return  {
      selectedView: String
    }
  },
  created(){
    this.selectedView = "home";
  },
  methods:{
  onButtonClicked(e) {
        this.selectedView = null;
        setTimeout(()=>{
          this.selectedView=e;
        },1100);
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Fira+Sans');
body{
  overflow-x: hidden;
  background-color: #141311;
}
</style>
