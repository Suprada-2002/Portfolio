<script>
    import Icon from '@iconify/svelte';
    let links = [
        {
          icon: "skill-icons:github-dark",
          href: "/"
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
            <p>Open Source | @SupradaTripathy | KISS</p>
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
    background-color: #111;
  }
  .footer-links{
    margin: 20px 0px;
  }
</style>