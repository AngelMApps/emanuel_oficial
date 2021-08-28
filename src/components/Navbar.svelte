<script>
    import { routes } from "./routes";
    import { url } from "@roxi/routify";
    import {meetLinks} from "./meeting_links"
    let nColor = 0;
    let sReuLinks=false;
    window.onscroll = () => {
        var scroll = document.documentElement.scrollTop || document.body.scrollTop;
        if (scroll >= 200) {
            nColor = 1;
            console.log(scroll);
        } else {
             nColor = 0;
          }
        };
    let showReuLinks = () =>{
        sReuLinks = !sReuLinks;
    };
    console.log(meetLinks[meetLinks.length-1].name);
</script>

<!-- markup (zero or more items) goes here -->
<nav class={nColor === 0 ? "transparent_nav" : "blur_nav"}>
  <div class="nav-div">
    <a class="title" href={$url(routes[0].route)}>{routes[0].name}</a>
    <ul>
      {#each routes as route}
        {#if route.name != "Iglesia Emanuel"}
            <li>
                {#if route.name !="Reuniones"}
                     <a class="routes" href={$url(route.route)}>{route.name}</a>
                 {:else}
                     <div class="list-meet" 
                         on:click={showReuLinks}>
                         <strong class="routes reu">{route.name}</strong>
                         <i class="fas fa-sort-down"></i>
                     </div>
                {/if}
            </li>
        {/if}
        
      {/each}
    </ul>
  </div>
</nav>
<ul class={sReuLinks ? "sidenav":"no_sidebar"}>
    {#each meetLinks as mt }
        <li on:click={showReuLinks}><a href={mt.route}>{mt.name}</a></li>
        {#if mt.index < 5}
            <hr/>
        {/if}
        <hr/>
    {/each}
</ul>
<style>
    @import url("https://fonts.googleapis.com/css2?family=Oswald:wght@600&display=swap");
    @import url("https://fonts.googleapis.com/css2?family=Lobster&display=swap");
    nav {
        z-index: 2;
        position: fixed;
        top: 0;
        margin: 0;
        padding: 0;
        left: 0;
        right: 0;
        height: 4rem;
    }
    hr{
        border: none;
        width: 100%;
        height: 0.05rem;
        background-color: rgba(255,255,255,0.1);
    }

    .sidenav{
        position: fixed;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 10rem;
        background:rgba(14, 15, 18,1);
        backdrop-filter: blur(200px);
        top: 4rem;
        left: calc(50% + 13.5rem);
        z-index: 2;
    }
    .sidenav a{
        padding: 5px;
        font-size: 14px;
        text-align: center;
        font-family: Helvetica, sans-serif, Arial;
        text-transform: uppercase;
    }
    .transparent_nav {
        background: transparent;
    }
    .blur_nav {
        background: rgba(0, 0, 0, 0.7);
        backdrop-filter: blur(200px);
     }
     .nav-div {
        padding: 10px 5px;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
     }
     .title {
        font-size: 35px;
        font-family: "Lobster", "Oswald", Helvetica, sans-serif, Arial, sans-serif;
     }
     .list-meet{
        display: flex;
        flex-direction: row;
        align-items: center;
    }
    i{
        margin-left: 0.4rem;
    }
    a,.list-meet {
        text-decoration: none;
        color: #fff;
        transition: color 1s;
    }
    strong{
        font-weight: 100;
    }
    a:hover {
        color: rgba(148, 178, 185,0.3);
        transition: color 1s;
        cursor: pointer;
    }
    .list-meet:hover{
        color: rgba(131, 152, 223,0.8);
        transition: color 1s;
        cursor: pointer;
    }


  ul {
    padding: 0;
    display: flex;
    flex-direction: row;
    width: 40%;
    justify-content: space-evenly;
    list-style: none;
  }
  .routes {
      font-size: 30px;
  }
</style>
