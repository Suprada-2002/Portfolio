<script>
    import Icon from "@iconify/svelte";
    import Navbar from "./Navbar.svelte";
    import {spring} from 'svelte/motion';

    let link =[
        {
            name:"India",
            link: "material-symbols:location-on"
        },
        {
            name: "16 March",
            link: "ic:sharp-cake"
        }
    ]

    const y = spring(0, {
		stiffness: 1,
		damping: 1,
	});

</script>

<svelte:head>
	<title>Suprada Tripathy - Student by day, developer by night.</title>
</svelte:head>

<div class="container">
    <div class="upper">
        <img src="../../../sunset.jpg" class="imgUpper" alt="sunset"
        style="position: 50% {$y}px"
        />
    </div>
</div>

<div class="container extra">
    <div class="lower">
        <img src="../../../profile.jpg" class="imgLower" alt="me" />
    </div>

    <h3>Suprada Tripathy</h3>
   <p>Web/.NET Developer | Student</p>

    <div class="links">
        <ul>
        {#each link as {name,link}}
       <li>
        <Icon icon={link} />
        <span>{name}</span>
       </li>
        {/each}
    </ul>
    </div>
</div>
<Navbar />

<style>
    .container{
        color: hsl(0, 0%, 80%);
        padding: 15px 0px;
    }
    p{
        padding: 10px 0px;
        font-weight: 400;
    }
    h3{
        font-weight: 700;
        font-size: 30px;
    }
    ul{
        display: flex;
        list-style: none;
        margin: 0px;
        gap:20px
    }
    li{
        margin: 0;
        padding: 10px 0px;
    }
   .imgUpper{
    border-radius: 0.25rem;
    width: 100%;
    height: 15rem;
    object-fit: cover;
    z-index: -50;
   }
   .upper{
    position: relative;
   
   }
   .lower{
    border-radius: 9999px;
    overflow: hidden;
    width: 7rem;
    z-index: 50;
    position: relative;
   }
   .imgLower{
    max-width: 100%;
    height: auto;
    display: block;
   }
   .extra{
    margin-top: -5rem;
    z-index: 10;
    padding-left: 3rem;
    padding-right: 3rem;
   }
</style>