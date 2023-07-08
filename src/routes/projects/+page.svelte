<script>
    let visualizationProject = [
        {
            name:"Suduko Visualization using Back-Tracking Algorithm",
            href:"/first",
        },
        {
            name:"Sorting Algorithm Visualizer",
            href:"/two",
        },
        {
            name:"Snake Game Visualization using A * search Algorithm",
            href:"/three",
        }
    ]

    let projects = [
        {
            name:"Know Your Couse",
            href:"/four"
        },{
            name:"CRUD Application using .NET core",
            href: "five"
        },{
            name:"Blog Application using React and Firebase",
            href: "/six"
        }
    ]
</script>

<div class="container">
    <h3><span>Visualization Projects</span></h3>
    <div class="visualization">
        {#each visualizationProject as {name, href} }
        <div class="project">
            <p>{name}</p>
            <a {href}>Know More</a>
        </div>
        {/each}
    </div>

    <h3><span>CRUD/Full Stack Projects</span></h3>
    <div class="visualization">
        {#each projects as {name, href} }
        <div class="project">
            <p>{name}</p>
            <a {href}>Know More</a>
        </div>
        {/each}
    </div>
</div>

<style>
    .container{
        text-align: center;
    }
    .visualization{
        display: flex;
        flex-wrap: wrap;
        gap:10px;
    }
    .project{
        width: 200px;
        height: auto;
        padding: 10px 10px;
        text-align: center;
        font-weight: 300;
        background-color: #111;
        border-radius: 10%;
    }
    a{
        text-decoration: none;
        color: orange;
        cursor: pointer;
        background-color: #111;
    }
    a:hover{
        color: blue;
    }
    p{
        background-color: #111;
    }
    h3{
        padding: 20px 0px;
    }
    span{
        font-weight: 300;
        border-bottom: 2px solid #111;
    }

</style>