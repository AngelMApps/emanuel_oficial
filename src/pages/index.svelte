<script>
  import InfoSection from "../components/home/info.svelte";
  import Footer from "../components/footer.svelte";
  import CompSocial from '../components/social_component.svelte';
  import CompParallax from '../components/parallax_comp.svelte';
</script>

<!-- markup (zero or more items) goes here 'about' -->
<main>
  <div class="container-top__home">
    <h1>BIENVENIDOS</h1>
    <div><h3>Somos la iglesia Emanuel</h3></div>
    <CompSocial/>
  </div>
  <CompParallax iURL="../images/fondo2.jpg" sHeight=40 sPadding=10/>
  <InfoSection/>
  <CompParallax iURL="../images/fondo3.jpg" sHeight=35 sPadding=0/>
  <Footer/>
</main>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Oswald:wght@600&display=swap");
   div{
    width: 100%;
  }
  .container-top__home {
    position: absolute;
    display: flex;
    flex-direction: column;
    align-items: center;
    top: 250px;
    left: 0;
    right: 0;
    z-index: 1;
    line-height: 2pt;
  }
  h1 {
    color: #fff;
    font-size: 80pt;
    font-family: "Oswald", Helvetica, sans-serif, Arial, sans-serif;
  }
  h3 {
    color: #fff;
    font-weight: 100;
    font-size: 20pt;
    text-align: center;
  }
</style>
