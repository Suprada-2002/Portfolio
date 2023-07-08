<script>
import Icon from "@iconify/svelte"

    let frontend = ["FrontEnd : ", "React.js", "Svelte.js/Kit", "Next.js", ".NET Core"];
    let backend = ["BackEnd : ","MySQL", "PostgreSQL", "Firebase", "Supabase"];
    let lang = ["Languages : ","C", "C++","C#","Java", "Python", "JavaScript", "HTML5", "CSS"]

    let techstackFirst = ["logos:react","logos:firebase","devicon:materialui","logos:visual-studio-code", "logos:figma" ]
    let techstackSecond = ["skill-icons:dotnet", "logos:angular-icon", "logos:mysql", "logos:bootstrap", "logos:visual-studio"]
    let techstackThird = ["vscode-icons:file-type-maven", "logos:java", "devicon:spring-wordmark", "devicon:eclipse"]
</script>

<div class="container">
    <div class="frontend skills">
        <ul>
        {#each frontend as name}
        <li>{name}</li>
        {/each}
        </ul>
    </div>

    <div class="backend skills">
        <ul>
            {#each backend as name}
            <li>{name}</li>
            {/each}
            </ul>
    </div>

    <div class="lang skills">
        <ul>
            {#each lang as name}
            <li>{name}</li>
            {/each}
            </ul>
    </div>
</div>

<div class="container">
    <p>Tech Stack I can Work With</p>
    <div class="tech-stack ">
        <div class="one">
                {#each techstackFirst as name}
                <Icon icon={name} width="30px" />
                {/each}
        </div>
        <div class="two">
                {#each techstackSecond as name}
                <Icon icon={name} width="30px" />
                {/each}
        </div>
        <div class="three">
            {#each techstackThird as name}
            <Icon icon={name} width="40px" />
            {/each}
    </div>
    </div>
</div>

<style>
    .container{
        display: block;
        text-align: center;
    }

    .skills{
        border: 10px;
        margin: 20px 0px;
        font-weight: 300;
    }
    ul{
        background-color: #111;
        list-style: none;
        display: flex;
        gap: 10px;
        padding: 15px 10px;
    }
    li{
        background-color: #111;
        margin: 0px;
        padding: 0px;
    }
    .tech-stack {
        display: flex;
       flex-wrap: wrap;
       gap: 20px;
    }
    .one, .two , .three {
        padding: 0px;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 20px;
        border: 1px solid #111;
    }
    p {
       font-weight: 300;
       border-bottom: 1px solid #111;
       margin: 40px 0px;
    }
</style>
