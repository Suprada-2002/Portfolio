<script>
     import { page } from "$app/stores";
    let navs = [
        {
            name: "About Me",
            href: "/"
        },
        {
            name: "Projects",
            href: "/projects"
        },
        {
            name: "Skills",
            href: "/skills"
        },
        {
            name: "Experience",
            href: "/exp"
        }
    ]
    $: routeId = $page.url.pathname;
</script>

<div class="container">

    <ul>
        {#each navs as {name, href}}
        <li><a {href}  class:active={routeId == href} >{name}</a></li>
        {/each}
    </ul>

</div>
<style> 
 ul{
    list-style: none;
    display: flex;
    gap:10px;
    justify-content: center;
 }
 a{
    text-decoration: none;
    font-weight: 300;
 }
 li{
    margin: 0px;
   
 }
  .active{
    
    border-bottom: 2px solid blue; 
  }
  </style>