<script>
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
</script>

<div class="container">

    <ul>
        {#each navs as {name, href}}
        <li><a {href}>{name}</a></li>
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
 a:hover {
    border-bottom: 3px solid #111;
  }
  </style>