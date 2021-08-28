<script>
    import CompSocial  from './social_component.svelte'
</script>

<footer>
    <div>
        <a class="div-number" href="tel:+51984135388">
            <i class="fas fa-phone-alt"/>
            <h5>984135388</h5>
        </a>   
    </div>
    <h4>
        Dios te trajo y nosotros te recibimos con amor
    </h4>
    <div class="div-social">
        <CompSocial marginTop={0}/>
    </div>
</footer>

<style>
    .div-number{ 
        margin-left: 5px;
        color: #fff;
        transition: color 1s;
        display: flex;
        flex-direction: row;
        align-items: center;
        text-decoration: none;
    }
    h4{
        color: #fff;
    }
    h4,h5{
        font-size: 30px; 
    }
    .fas{
        margin-right: 5px;
        font-size: 25px;
    }
    .div-number:hover{
        color: rgba(148, 178, 185,0.3);
        transition: color 1s;
    }
    footer{
        padding:5px;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        bottom: 0;
        z-index: 1;
        height: 4rem;
        background-color: #000;
    }
    .div-social{
        display: flex;
        flex-direction: column;
        justify-content: center;
        width: 10%;
    }
</style>
