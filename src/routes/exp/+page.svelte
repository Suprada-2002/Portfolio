<script>

    let expList = [
        {
            name: "Associate Software Intern",
            company:"Highradius Corporation",
            time:"Jun 2022 - Apr 2023",
            skills: "Java, React.js, Spring Boot, Maven, MUI ",
            list: [
                "Used React.js and Ext.js for UI",
                "Java using MVC architecture",
                "spring boot and maven",
                "exsential team building skill"
            ]
        },
        {
            name: "Data Analyst Intern",
            company:"Lagazon EduTech",
            time:"Jan 2022 - Apr 2022",
            skills: "Power BI, Data Visualization, Data Cleaning ",
            list: [
                "Data Visualization using PowerBI",
                "Introduction to Machine Learning ",
                "Numpy and Python",
                "Leadership skill"
            ]
        }
    ]
</script>

<div class="container">

    {#each expList as {name, company ,skills, time, list}}
    <div class="exp">
        <p><span>{name}</span></p>
        <p class="blue">{company} ( <i>{time} </i> )</p>
        <p>Skills : {skills}</p>
            {#each list as li}
            <li>{li}</li>
            {/each}
     </div>
    {/each}
</div>

<style>
    .container{
        padding: 10px 0px;
    }
    .exp{
        margin-top: 20px;
        border: 2px solid #111;
        padding-left: 10px;
        padding-top: 10px;
        padding-bottom: 10px;
        font-weight: 300;
    }
    span{
        font-weight: 400;
        border-bottom: 2px solid blue;
    }
    i{
        font-size: 10px;
    }
</style>