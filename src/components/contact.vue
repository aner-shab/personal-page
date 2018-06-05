<template>  
<div>
  <ul class="belt">
     <li class="button">
          <a href="https://github.com/aner-shab/">
          <div class="icon icon-github"></div>
          </a>
          <span class="tag">Github</span>
      </li>
     <li class="button">
          <a href="mailto:aner.shab@gmail.com">
          <div class="icon icon-mail"></div>
          </a>
          <span class="tag">Mail</span>
      </li>
     <li class="button">
          <a href="https://corvian.net/CV_Aner_Shab.pdf">
          <div class="icon icon-cv"></div>
          </a>
          <span class="tag">CV</span>
      </li>
    </ul>
</div>
</template>

<script>
export default {
  name: 'Contact',
    data:function() {
    return  {
      currentNumber: 0,
      images: [
        require('../assets/cv.png'),
        require('../assets/mail.svg')
      ]
    }
  },
  props: {
  },
  methods: {
  },
  created: function(){
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
*{
  font-family: 'Fira Sans', sans-serif;
  color: #b2b2b2;
}
ul{
text-align: center;
padding-left:0px;
}
ul li {
  display: inline;
}


.belt{
  margin-top: 230px;
}
.button{
  width: 150px;
  height: 156px;
  cursor: pointer;
  display: inline-block;
  margin-right: 50px;
  margin-left: 50px;
  margin-top:20px;
}
.icon{
  vertical-align: middle;
  background-size: contain;
  width: 150px;
  height: 150px;
  background-repeat:no-repeat;
  opacity: 0.8;
  margin-bottom:10px;
}
.icon:hover{
    transition: 1s;
    transform: rotate(-360deg);
}
.icon-github{
  background-image: url("../assets/github.png");
}
.icon-cv{
  background-image: url("../assets/cv.png");
}
.icon-mail{
  background-image: url("../assets/mail.svg");
}

@media (max-width: 1050px) {
.belt{
  margin-top: 230px;
}
  .button{
    width: 150px;
    height: 156px;
  }
  .icon{
    width: 150px;
    height: 150px;
  }
}
@media (max-width: 800px) {
.belt{
  margin-top: 230px;
}
  .button{
    width: 150px;
    height: 156px;
  }
  .icon{
    width: 150px;
    height: 150px;
  }
}
@media (max-width: 650px) {
.belt{
  margin-top: 70px;
}
  .button{
    width: 100px;
    height:106px;
  }
  .icon{
    width: 100px;
    height: 100px;
  }
}
@media (max-width: 350px) {
  .belt{
    margin-top: 70px;
  }
  .button{
    width: 100px;
    height:106px;
  }
  .icon{
    width: 100px;
    height: 100px;
  }
}

</style>
