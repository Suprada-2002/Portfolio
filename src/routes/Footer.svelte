<script>
    import Icon from '@iconify/svelte';
    let links = [
        {
          icon: "skill-icons:github-dark",
          href: "https://github.com/Suprada-2002?tab=repositories"
        },{
            icon: "skill-icons:linkedin",
            href: "/"
        },{
            icon: "logos:google-gmail",
            href: "/"
        },{
            icon:"logos:chrome-web-store",
            href:"/"
        },{
            icon:"skill-icons:instagram",
            href: "/"
        }

    ]
</script>

    <footer class="container">
        <div class="footer-links">
            <ul>
                {#each links as {icon, href}}
                <li><a {href}><Icon icon={icon} /></a></li>
                {/each}
            </ul>
        </div>
        <div class="content">
            <p>Made with 💝 and Svelte</p>
            <p><a href="https://en.wikipedia.org/wiki/Open_source">Open Source</a> | @SupradaTripathy | <a href="https://en.wikipedia.org/wiki/KISS_principle">KISS</a></p>
        </div>
    </footer>


<style>
   footer{
        text-align: center;
        padding: 10px 10px;   
    }
    p{
        font-weight: 300;
    }
    ul{
        display: flex;
        align-items: center;
        gap:20px;
        list-style-type: none;
        justify-content: center;
    }
    li, a, ul{
        margin: 0px;
        padding: 0px;
        cursor: pointer;
    }

  a:hover {
    color: orange;
  }
  a{
    text-decoration: none;
    cursor: pointer;
  }
  .footer-links{
    margin: 20px 0px;
  }
  .content{
    margin: 10px 0px;
  }
</style>