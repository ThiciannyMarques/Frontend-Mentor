<template>

  <div id="app">
    <header >
        <nav>
            <div class="navbar">
              <div class="logo">
                <a href="#" >
                   <img src="../src/assets/logo.svg" alt=""> 
                </a>
              </div>
              <div class="link">
                <a href="home"> Home </a>
                <a href="#sobre"> Sobre </a>
                <a href="#projetos"> Projetos </a>
                <a href="#contato"> Contato </a>
              </div>
            </div>  
            <div class="nav-text">
              <span>Thicianny Marques</span>
            </div> 
        </nav>
    </header>
    <main>

      <h1 id="sobre">Sobre</h1>
      <div  class="principal">
        <div class="principal-img">
          <img src="https://raw.githubusercontent.com/ThiciannyMarques/Frontend-Mentor/master/8-huddle-landing-page-with-single-introductory-section-master/design/desktop-preview.jpg" alt="">
        </div>
        <div class="principal-text">
          <span>
            Projetos do Frontend Mentor
          </span> 

          <p>
            Projetos que pus em pratica minha habilidades em Frontend. Feitos com HTML, CSS e JAVASCRIPT, os projetos que vão além de tela de perfil, card groups, calculadora e ladding pages.
          </p> 
        </div>
      </div>

        <h1 id="projetos">Projetos</h1>
      <div  class="projetos " data-flickity-options='{ "wrapAround": true }'>   
        <div v-for="row in projetos" :key="row.link">
          <a :href="row.link">
            <div class="card">
              <img :src="row.img" alt="">
              {{row.nome}}
            </div>
          </a>
         
        </div>
      </div>
      <div id="contato">
        <h1>Contato</h1>
        <ul>
          <li>Celular: (91)984399335</li>
          <li>Email: Thicianny14@gmail.com</li>
          <li>Linkedin: adasd</li>
          <li>Github: affafsadf</li>
          <li>Portfolio: wafsgghgjklkhjk</li>
        </ul>
      </div>
      <footer>
        copyrigth
      </footer>
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
            nome: "Order Sumare",
            img: "https://raw.githubusercontent.com/ThiciannyMarques/Frontend-Mentor/master/1-order-summary-component-main/design/desktop-preview.jpg", link:"https://order-summary-component-main-steel.vercel.app"
          } ,
           {
            nome: "Status Preview Card",
            img: "https://raw.githubusercontent.com/ThiciannyMarques/Frontend-Mentor/master/2-stats-preview-card-component-main/design/desktop-preview.jpg", link:"https://order-summary-component-main-steel.vercel.app"
          } ,
           {
            nome: "Column Preview Card",
            img: "https://raw.githubusercontent.com/ThiciannyMarques/Frontend-Mentor/master/3-column-preview-card-component-master/design/desktop-preview.jpg", link:"https://order-summary-component-main-steel.vercel.app"
          },
           {
            nome: "Profile Card",
            img: "https://raw.githubusercontent.com/ThiciannyMarques/Frontend-Mentor/master/4-profile-card-component-main/design/desktop-preview.jpg", link:"https://order-summary-component-main-steel.vercel.app"
          },
           {
            nome: "Social Proof",
            img: "https://raw.githubusercontent.com/ThiciannyMarques/Frontend-Mentor/master/5-social-proof-section-master/design/desktop-preview.jpg", link:"https://order-summary-component-main-steel.vercel.app"
          } ,
           {
            nome: "Four Card Feature",
            img: "https://raw.githubusercontent.com/ThiciannyMarques/Frontend-Mentor/master/6-four-card-feature-section-master/design/desktop-preview.jpg", link:"https://order-summary-component-main-steel.vercel.app"
          },
           {
            nome: "Single Price Grid",
            img: "https://raw.githubusercontent.com/ThiciannyMarques/Frontend-Mentor/master/7-single-price-grid-component-master/design/desktop-preview.jpg", link:"https://order-summary-component-main-steel.vercel.app"
          },
           {
            nome: "Huddle Landing Page With Single Introductory",
            img: "https://raw.githubusercontent.com/ThiciannyMarques/Frontend-Mentor/master/8-huddle-landing-page-with-single-introductory-section-master/design/desktop-preview.jpg", link:"https://order-summary-component-main-steel.vercel.app"
          } ,
           {
            nome: "Base Apparel Coming Soon",
            img: "https://raw.githubusercontent.com/ThiciannyMarques/Frontend-Mentor/master/9-base-apparel-coming-soon-master/design/desktop-preview.jpg", link:"https://order-summary-component-main-steel.vercel.app"
          },
           {
            nome: "Tip Calculator App",
            img: "https://raw.githubusercontent.com/ThiciannyMarques/Frontend-Mentor/master/10-tip-calculator-app-main/design/desktop-preview.jpg", link:"https://order-summary-component-main-steel.vercel.app"
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
  a{
    color: white;
    text-decoration: none;
  }
  h1{
    margin-top: 10%;
    margin-bottom: 5%;
  }
  body {
    padding: 0px;
    margin: 0px;
    
  }



  nav{ 
    background-image: url('https://kinsta.com/pt/wp-content/uploads/sites/3/2020/02/praticas-web-design-proximo-projecto.jpg');
    color: hsl(0, 0%, 100%);
    height: 700px;
    background-attachment: fixed;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
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
    padding: 0% 10% 0% 10%;
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
    width: 80%;
    margin: 0% 10% 0% 14%;
  }
  .card{
    font-size: 18px;
    font-family: 'Alata', sans-serif; 
    color: rgb(115, 115, 126);
    background-color: rgba(196, 196, 196, 0.199);
    padding: 0% 5% 5% 5%;
    border-radius: 15px;
    width: 70%;
    height: 230px;
    margin-right: 10px;
    counter-increment: card;
  }
  .card img{
    width: 100%;
  }

  #contato ul{
    text-align: left;
    
  }
  #contato ul li{
    margin-top: 2%;
    text-decoration: none;
  }
  footer{
    width: 100%;
    padding: 1%;
    background-color: blue;
    color: white;
  }

</style>
