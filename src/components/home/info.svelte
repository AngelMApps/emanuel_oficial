<script>
  // your script goes here
</script>

<!-- markup (zero or more items) goes here -->

<div class="div-info">
  <p>
    Nuestra misión como iglesia es llevar el mensaje de salvación 
    y mostrar el amor de Dios a todas las personas. 
  </p>
  <img alt="logo" src="../images/logo.png"/>
</div>

  
<style>
  div{
      display:flex;
      flex-direction:column;
      justify-content:center;
      align-items: center;
      
      
  }
  .div-info{
    left: 15%;
    right: 15%;
    position: absolute;
    z-index: 1;
    height: 25rem;
    border-radius: 35px;
    padding: 2.5rem;
    margin-top: 6rem;
    background-color: rgba(129, 188, 218, 0.1);
    box-shadow: -1px 2px 2px 2px rgba(0, 0, 0, 0.2);
  }
  p{
      color: #fff;
      text-align: center;
      font-size: 30px;
      padding-top: 2rem;
      font-weight: 200;
  }
  img{
    height: 20rem;
  }
</style>
