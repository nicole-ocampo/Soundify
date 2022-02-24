<template>
  <div id="realmain">
    <div id="main">
    
      <!-- Navbar -->
      <div id="navbarcontainer">
        <a href="#containerone" @click="cont1"> <div class="navbarbutton" id="cont1nav"></div> </a>
        <a href="#containertwo" @click="cont2"> <div class="navbarbutton" id="cont2nav"></div> </a>
        <a href="#containerthree" @click="cont3"> <div class="navbarbutton" id="cont3nav"></div> </a>
        <a href="#containerfour" @click="cont4"> <div class="navbarbutton" id="cont4nav"></div> </a>
        <a href="#containerfive" @click="cont5"> <div class="navbarbutton" id="cont5nav"></div> </a>
      </div>

      <!-- Container 1 -->
      <div id="containerone">
        <div id="imgcontainer">
          <img src="@/assets/musichome.png">
        </div>
        <div class="titlecontainer">
          <div id="headerTitle"> Hello </div> 
          <div id="subTitle"> 
              Your favourite music app is now here. This is a placeholder text because I do not 
              know what to put here.  <br> 
          
              <button class="controlButton" id="getStarted">Get Started</button>
          </div>
        </div>
      </div>

      <!-- Container 2 -->
      <!-- Top Artists -->
      <div id="containertwo">
        
        <div id="artistheader"> Featuring your favourite artists! </div>


        <div id="artistcontainer">
          <div class="artistdesccont">
            <div class="artistdesc" id="artist1">
              <img src="@/assets/menitrust.jpg">
              <div class="artisttext">
                <div class="artisttitle"> Men I Trust </div> <br>
                <div class="artistsub"> Men I Trust is a Canadian indie band from Montreal, Quebec. Formed in 2014, the band consists of Jessy Caron, Dragos Chiriac, and Emmanuelle Proulx. The group self-released their early work and subsequently published music on Canadian indie label Return to Analog. </div>
              </div>
            </div>
            
            <div class="artistdesc" id="artist2">
              <img src="@/assets/themarias.jpg">
              <div class="artisttext">
                <div class="artisttitle"> The Marias </div> <br>
                <div class="artistsub"> The Marías are an indie pop band composed of Puerto Rican lead singer María Zardoya and drummer Josh Conway. They are known for performing songs in English and Spanish, as well as infusing their music with elements like jazz percussion, guitar riffs, smoke-velvet vocals, and horn solos. </div>
              </div>
            </div>




          </div>
          <div class="artistdesccont">

            <div class="artistdesc" id="artist3">
              <img src="@/assets/vaundy.jpg">
              <div class="artisttext">
                <div class="artisttitle"> Vaundy </div> <br>
                <div class="artistsub"> Vaundy (バウンディ) is a Japanese singer-songwriter, composer, producer and designer. </div>
              </div>
            </div>

            <div class="artistdesc" id="artist4">
              <img src="@/assets/arcticmonkeys.jpg">
              <div class="artisttext">
                <div class="artisttitle"> Arctic Monkeys </div> <br>
                <div class="artistsub"> Arctic Monkeys are an English rock band formed in Sheffield in 2002. The group consists of Alex Turner, Jamie Cook, Nick O'Malley, and Matt Helders. Former band member Andy Nicholson left the band in 2006 shortly after their debut album was released. </div>
              </div>
            </div>

          </div>
        </div>
      </div>

      <!-- Container 3 -->
      <!-- Moving numbers -->
      <div id="containerthree">
      </div>

      <!-- Container 4 -->
      <!-- Play song + moving lyrics? -->
      <div id="containerfour">
      </div>

      <!-- Container 5 -->
      <!-- Start now. -->
      <div id="containerfive">
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods: {
    cont1: function(){
      document.getElementById("cont2nav").style.backgroundColor = "transparent";
      document.getElementById("cont3nav").style.backgroundColor = "transparent";
      document.getElementById("cont4nav").style.backgroundColor = "transparent";
      document.getElementById("cont5nav").style.backgroundColor = "transparent";

      document.getElementById("cont1nav").style.backgroundColor = "white";
  },
    cont2: function(){
      document.getElementById("cont1nav").style.backgroundColor = "transparent";
      document.getElementById("cont3nav").style.backgroundColor = "transparent";
      document.getElementById("cont4nav").style.backgroundColor = "transparent";
      document.getElementById("cont5nav").style.backgroundColor = "transparent";

      document.getElementById("cont2nav").style.backgroundColor = "white";
    },
    cont3: function(){
      document.getElementById("cont1nav").style.backgroundColor = "transparent";
      document.getElementById("cont2nav").style.backgroundColor = "transparent";
      document.getElementById("cont4nav").style.backgroundColor = "transparent";
      document.getElementById("cont5nav").style.backgroundColor = "transparent";

      document.getElementById("cont3nav").style.backgroundColor = "white";
    },
    cont4: function(){
      document.getElementById("cont1nav").style.backgroundColor = "transparent";
      document.getElementById("cont2nav").style.backgroundColor = "transparent";
      document.getElementById("cont3nav").style.backgroundColor = "transparent";
      document.getElementById("cont5nav").style.backgroundColor = "transparent";

      document.getElementById("cont4nav").style.backgroundColor = "white";
    },
    cont5: function(){
      document.getElementById("cont1nav").style.backgroundColor = "transparent";
      document.getElementById("cont2nav").style.backgroundColor = "transparent";
      document.getElementById("cont3nav").style.backgroundColor = "transparent";
      document.getElementById("cont4nav").style.backgroundColor = "transparent";

      document.getElementById("cont5nav").style.backgroundColor = "white";
    }
  }
}
</script>

<style scoped>

/* Animations */
@keyframes gradient {
  0% {
      background-position: 0% 50%;
  }
  50% {
      background-position: 100% 50%;
  }
  100% {
      background-position: 0% 50%;
  }
}

@keyframes slide-up {
  0% {
    transform: translateY(100%);
  }
  100% {
    transform: translateY(0);
  }
}

@keyframes slide-left {
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(0);
  }
}

/* Components */
#realmain{
  background-color: #001004;
  position:fixed;
  width:100%;
  height:140%;
  margin-top:-10%;
  display:flex;
  justify-content:center;
}

#main{
  margin-top:2.5%;
  background: linear-gradient(-45deg, #ddd78d, #dcbf85, #8b635c, #93a29b);
  animation: gradient 15s ease infinite;
  background-size: 400% 400%;
  width:95%;
  height:90%;
  border-radius:50px;
  position:fixed;
  top:0%;
  overflow:scroll;
  overflow-x:hidden;
  scroll-behavior: smooth;
}

#navbarcontainer{
  margin:0;
  float:right;
  position:fixed;
  margin-top:21%;
  right:6%;
  width:20px;
  height:100px;
  z-index:9;
}

.navbarbutton{
  border-radius:360px;
  width:15px;
  height:15px;
  border:1px solid #fff;
  margin-top:5px;
  transition: all 0.01s ease-in;
}

#cont1nav{
  background:white;
}

.navbarbutton:hover{
  background:white;
  transition: all 0.01s ease-in;
}

#containerone{
  width:100%;
  height:100%;
  display:flex;
  justify-content: flex-start;
  position:relative;
  overflow:hidden;
}

#containertwo{
  width:100%;
  height:100%;
  background:#8b635c;
}

#containerthree{
  width:100%;
  height:100%;
  background:#dcbf85;
}

#containerfour{
  width:100%;
  height:100%;
  background:#ddd78d;
}

#containerfive{
  width:100%;
  height:100%;
  background:#60594d;
}

/* Container 1 elements */

.titlecontainer{
  width: 700px;
  display: block;
  margin-top: 20%;
  position:relative;
  animation: slide-up 1.5s cubic-bezier(0.2, 0, 0.2, 1) 500ms;
}

#imgcontainer{
  display: block;
  width:900px;
  margin:0;
  margin-left:0.1%;
  margin-top:1%;
  animation: slide-left 1.5s cubic-bezier(0.2, 0, 0.2, 1) 500ms;
  position:relative;
  opacity:0.75;
  object-fit:cover;
}
#headerTitle{
  margin-left: auto; 
  margin-right: 0;
  float:left;
  font-family: 'Montserrat', sans-serif;
  font-size:100px;
  color: #fff;
  width: inherit;
  text-align:left;
  font-weight: bold;
}

#subTitle{
  margin-left: auto; 
  margin-right: 0; 
  float:left;
  font-family: 'Open Sans', sans-serif;
  font-size: 20px; 
  width: 600px;
  text-align:left;
  color:#fff;
}

.controlButton{
  margin-left: auto; 
  margin-right: 0;
  margin-top:20px;
  float:left;
  font-family: 'Open Sans', sans-serif;
  font-size: 15px;
  color: #fff;
  background:transparent;
  border: 1px solid #fff;
  padding: 15px;
  border-radius:100px; 
}

.controlButton:hover{
  animation: ease-in-out 0.5s;
  background:#fff;
  color:#a8a8a8;
}

/* Container 2 elements */
#artistcontainer{
  margin:0%;
  display:block;
  height:100%;
  width:100%;
  padding:100px;
  display:flex;
  justify-content:space-evenly;
  flex-direction:column;
  animation: slide-up 1.5s cubic-bezier(0.2, 0, 0.2, 1) 500ms;
  animation-delay: 1s;
}

#artistheader{
  font-family: 'Rock Salt', cursive;
  font-size: 50px;
  margin-top:70px;
  margin-left: 40px;
  float:left;
  color:#fff;
  transform: rotate(-2deg);
}

.artistdesccont{
  display:flex;
  justify-content: space-evenly;
  flex-direction: row;
}

.artistdesc{
  width:800px;
  height:300px;
  padding:20px;
  padding-top:0px;
  margin-top:-3%;
  display:flex;
  flex-direction:row;
}

.artistdesc img{
  border-radius:20px;
  height:240px;
  width:240px;
  object-fit:cover;
  filter: brightness(80%) contrast(90%);
}

.artistdesc img:hover{
  border-radius:0px;
  transition:all 0.1s ease-out;
}

.artisttext{
  width:300px;
  text-align:left;
  color:#fff;
  margin-left:30px;
}

.artisttitle{
  font-family:'Montserrat', sans-serif;
  font-size:30px; 
  font-weight:bold;
}

.artistsub{
  font-family:'Open Sans', sans-serif;
  font-size:15px;
}

/* Scrollbar */
::-webkit-scrollbar {
  width: 0px;
}

::-webkit-scrollbar-track {
  background: transparent;
}

::-webkit-scrollbar-thumb {
  background: transparent;
}

::-webkit-scrollbar-thumb:hover {
  background: transparent;
}

</style>
