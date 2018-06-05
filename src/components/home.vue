<template>
  <div>
    <div class="name">
      <span class="logo">
        <span id="a" class="letter" @mouseover="$event.target.classList.add('hovered')" @animationend="$event.target.classList.remove('hovered')">A</span>
        <span id="n" class="letter" @mouseover="$event.target.classList.add('hovered')" @animationend="$event.target.classList.remove('hovered')">N</span>
        <span id="e" class="letter" @mouseover="$event.target.classList.add('hovered')" @animationend="$event.target.classList.remove('hovered')">E</span>
        <span id="r" class="letter" @mouseover="$event.target.classList.add('hovered')" @animationend="$event.target.classList.remove('hovered')">R</span>
      </span>
      <span class="logo">
        <span id="s" class="letter" @mouseover="$event.target.classList.add('hovered')" @animationend="$event.target.classList.remove('hovered')">S</span>
        <span id="h" class="letter" @mouseover="$event.target.classList.add('hovered')" @animationend="$event.target.classList.remove('hovered')">H</span>
        <span id="a2" class="letter" @mouseover="$event.target.classList.add('hovered')" @animationend="$event.target.classList.remove('hovered')">A</span>
        <span id="b" class="letter" @mouseover="$event.target.classList.add('hovered')" @animationend="$event.target.classList.remove('hovered')">B</span>
        <span id="t" class="letter" @mouseover="$event.target.classList.add('hovered')" @animationend="$event.target.classList.remove('hovered')">T</span>
        <span id="a3" class="letter" @mouseover="$event.target.classList.add('hovered')" @animationend="$event.target.classList.remove('hovered')">A</span>
        <span id="i" class="letter" @mouseover="$event.target.classList.add('hovered')" @animationend="$event.target.classList.remove('hovered')">I</span>
      </span>
    </div>
    
    <p>Hello!</p>
    <p>My name is <span class="highlight">Aner</span> (it says so right there!) and I am a <span class="highlight">full-stack developer</span> from a quaint little kibbutz in Israel.</p>
    <p>
    I have experience ranging from low-level system and automated solutions to mobile apps and front-end development.
    </p>
  </div>
</template>

<script>
export default {
  name: 'Home',
  props: {
  }
  
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>



p {
  cursor: default;
  margin-left: 40px;
  margin-bottom: -10px;
  color: #b2b2b2;
  font-family: 'Fira Sans', sans-serif;
  font-size: 20px;
}


.name {
  cursor: default;
  margin-top: 60px;
  margin-bottom: 30px;
  text-align: left;
  }

.logo {
  margin-left: 40px;
  display: block;
}
.letter {
  font-size: 200px;
  line-height: 110px;
  font-family: 'Fira Sans', sans-serif;
  font-weight: 800;
  letter-spacing: -20px;
  position: relative;
  transition: top ease 0.1s;
  transition-delay: 2s;
  opacity: 0.9;
  }

  
@media (max-width: 1050px) {
  .letter{
    font-size:200px;
    letter-spacing: -20px;
  }
  .logo{
    margin-left: 40px;
  }
  p{
    font-size: 20px;
    margin-left: 40px;
  }
}
@media (max-width: 800px) {
  .letter{
    font-size:150px;
    letter-spacing: -15px;
  }
  .logo{
    margin-left: 30px;
  }
  p{
    font-size: 20px;
    margin-left: 30px;
  }
}
@media (max-width: 650px) {
  .letter{
    font-size:100px;
    letter-spacing: -10px;
    line-height: 80px;
  }
  .logo{
    margin-left: 20px;
  }
  p{
    font-size: 20px;
    margin-left: 20px;
  }
}
@media (max-width: 350px) {
  .letter{
    font-size:80px;
    letter-spacing: -8px;
    line-height: 80px;
  }
  .logo{
    margin-left: 10px;
  }
  p{
    font-size: 18px;
    margin-left: 10px;
  }
}


#a {
  color: #586073;
}

#n {
  color: #868685;
}

#e {
  color: #494949;
}

#r {
  color: #232323;
}

#s {
  color: #586073;
}

#h {
  color: #b2b2b2;
}

#a2 {
  color: #868685;
}

#b {
  color: #494949;
}

#t {
  color: #232323;
}

#a3 {
  color: #494949;  
}

#i {
  color: #868685;  
}

.highlight{
  color: steelblue;
}

@keyframes letterBounce {
    0% {
      top: 0px;
    }
    50% {
      top: 50px;
    }
    100% {
      top: 0px;
  }
}
.hovered {
  animation: letterBounce 3s;
}

::selection {
  background: #b39ddb;
}

</style>
