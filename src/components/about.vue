<template>
  <div>
    <img class="pic" :src="currentImage" />
>
    <p>I am versed in:</p> <br>
    <ul class="skillist">
     <li>Javascript</li>
     <li>Typescript</li>
     <li>C#</li>
      <li>C++</li>
      <li>SQL</li>
      <li>Java</li>
      <li>Objective-C</li>
     </ul>
    <ul class="skillist">
     <li>Vue.js</li>
     <li>Angular 2+</li>
     <li>AngularJS</li>
     <li>React</li>
     <li>Ionic</li>
     <li>Cordova (PhoneGap)</li>
     <li>.NET</li>
     <li>.NET Core</li>
     <li>Spring</li>
     </ul>
    <ul class="skillist">
     <li>Jenkins</li>
     <li>Docker</li>
     </ul> 
     <br>
    <p>As well as:</p> <br>
    <ul class="skillist">
     <li>GIS & GNSS Systems</li>
     <li>Computer Vision</li>
     <li>CAD Software</li>
     <li>PLC Programming</li>
     </ul>
    <br>
   </div>
</template>

<script>
export default {
  name: 'About',
  props: {
  },
  data:function() {
    return  {
      currentNumber: 0,
      images: [
        require('../assets/me1.png'),
        require('../assets/me2.png')
      ]
    }
  },
  computed:{
    currentImage: function() {
      return this.images[Math.abs(this.currentNumber) % this.images.length];
      }
  },
  created(){
    this.currentNumber = Math.floor(Math.random() * 3) + 1  
  },
  methods:{
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
*{
  font-family: 'Fira Sans', sans-serif;
}
.skillist{
text-align: center;
}
ul{
  padding-left:0px;
  }
ul li {
  font-family: 'Consolas', sans-serif;
  display: inline-block;
  color: #b2b2b2;
  font-size: 16px;
  cursor: default;
}
ul li:not(:last-child):after {   
  content: "·";
   padding: 0 .3em; 
  }
li:hover{
  color:steelblue;
}
p {
text-align: center;
  cursor: default;
  margin-bottom: -10px;
  color: #b2b2b2;
  font-size: 20px;
}

img{
    object-fit: cover;
    display: block;
    margin: 0 auto;
    transition:opacity 1.5s linear;
}

.pic{
  width:300px;
  height:300px;
  border-radius: 50%;
  border: 15px solid #41516b;
  margin: 0 auto;
  margin-top:60px;
  margin-bottom: 20px;
}
.pic:hover{
    animation: pulse 1s;
}

@media (max-width: 1050px) {
  .pic{
    width:300px;
    height:300px;
  }
}
@media (max-width: 800px) {
  .pic{
    width:250px;
    height:250px;
  }
}
@media (max-width: 650px) {
  .pic{
    width:200px;
    height:200px;
  }
}
@media (max-width: 350px) {
  .pic{
    width:200px;
    height:200px;
  }
}

</style>
