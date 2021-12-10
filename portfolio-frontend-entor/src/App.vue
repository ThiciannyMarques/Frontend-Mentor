<template>

  <div id="app">
    <header >
        <nav>
            <div class="navbar">
              <div class="logo">
                <router-link>
                   <img src="../src/assets/logo.svg" alt=""> 
                </router-link>
              </div>
              <div class="link">
                <router-link> About </router-link>
                <router-link> Carrers </router-link>
                <router-link> Events </router-link>
                <router-link> Products </router-link>
                <router-link> Support </router-link>
              </div>
            </div>  
            <div class="nav-text">
              <span>IMMERSIVE EXPERIENCES THAT DELIVER</span>
            </div> 
        </nav>
    </header>
    <main>
      <div class="principal">
        <div class="principal-img">
          <img src="../src/assets/desktop/image-interactive.jpg" alt="">
        </div>
        <div class="principal-text">
          <span>
            The leader in interactive VR
          </span> 

          <p>
            Founded in 2011, Loopstudios has been producing world-class virtual reality 
            projects for some of the best companies around the globe. Our award-winning 
            creations have transformed businesses through digital experiences that bind 
            to their brand.
          </p> 
        </div>
      </div>

      <div class="projetos">   
        <div v-for="row in projetos" :key="row.link">
          <a :href="row.link">
            <div class="card">
              <img :src="row.img" alt="">
              {{row.nome}}
            </div>
          </a>
         
        </div>
      </div>
    </main>
  </div>
  
</template>

<script>
  //import Home from './components/Home.vue'
  //import NavBar from './components/NavBar.vue'

  export default {
    name: 'App',
    data(){
      return{
        name: "jorge",
        projetos: [
          {
            nome: "order sumare",
            img: "https://s2.static.brasilescola.uol.com.br/be/2020/12/peixe.jpg", link:"https://order-summary-component-main-steel.vercel.app"
          } 
        ]       
      }
    }
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Alata&display=swap');

  @import url('https://fonts.googleapis.com/css2?family=Alata&family=Josefin+Sans:wght@300&display=swap');


  *{
    box-sizing: border-box;
  }
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    font-family: 'Josefin Sans', sans-serif; 
  }
  body {
    padding: 0px;
    margin: 0px;
    
  }



  nav{ 
    background-image: url('assets/desktop/image-hero.jpg');
    color: hsl(0, 0%, 100%);
    height: 500px;
    
  }
  .navbar{
    width: 80%;
    margin: auto;
    padding: 50px 0;
  }
  .logo{
    float: left;
  }
  .link{
    float: right;
  }
  .link router-link{
    margin-right: 5px;
  }
  .nav-text{
    border: solid 1px white;
    margin: 5% 10%;
    padding: 2%;
    width: 35%;
    font-size: 50px;
    text-align: left;
  }



  .principal{
    display: flex;
    padding: 10%;
  }
  .principal-img{
    width: 40%;
  }
  .principal-text{
    background-color: rgb(252, 252, 252);
    height: 30%;
    margin-top: 15%;
    margin-left: 15%;
    padding: 10% 0 1% 7%;
    width: 60%;
    text-align: left;
  }
  .principal-text span{
    font-size: 36px;
    text-transform: uppercase;
  }
  .principal-text p{
    margin-top: 15%;
  }



  .projetos{
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 50px;
    margin: 30px;
    width: 80%;
    margin: auto;
  }
  .card{
    font-size: 18px;
     font-family: 'Alata', sans-serif; 
     background-color: rgba(141, 138, 133, 0.384);
     padding: 15%;
     border-radius: 15px;
  }
  .card img{
    width: 100%;
  }

</style>
