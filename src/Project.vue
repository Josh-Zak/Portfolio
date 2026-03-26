<template>
    <div class="projectContainer">
        <div class="projectLeft">
            <h3>{{ name }}</h3>
            <p>{{ desc }}</p>
            <div id="techStack">
                <div class="techStackNode" v-for="(tech, index) in stack" :key="index">
                    {{ tech }}
                </div>
            </div>
        </div>
        <div class="buttons">
            <a class="link" :href="link" target="_blank">Link</a>
            <a class="github" :href="github" target="_blank">GitHub</a>
        </div>
    </div>
</template>



<script>
export default{
    name: "Project",
    props:{
        name: String,
        desc: String,
        link: String,
        github: String,
        stack: Array
    }
}
</script>


<style>
.projectContainer{
    border: solid black;
    border-radius: 10px;
    padding: 2rem;
    display: flex;
    background-color: white;
}

.projectLeft{
    flex: 5;
}

.projectContainer .buttons{
    display: flex;
    flex-direction: column;
    gap: 1rem;
    align-items: center;
    padding-top: 2rem;
}

.projectContainer .buttons *{
    padding: 0.5rem 1rem;
    width: 100%;
    border: 2px solid black;
    border-radius: 1.25rem;
    text-decoration: none;
    text-align: left;
    font-size: 1.5rem;
    color: white;
    background-color: var(--secondary);
}

#techStack{
    display: flex;
    gap: 1rem;
}

.techStackNode{
    background-color: var(--secondary);
    color: white;
    padding: 0.5rem 1rem;
    border-radius: 1rem;
    font-size: 120%;
    width: 8%;
    text-align: center;
}

.projectContainer p{
    color: var(--tertiary);
    font-weight: bold;
}

.projectContainer h3{
    color: var(--secondary);
}



</style>