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
            <a class="link" :href="link" target="_blank">Visit Website ></a>
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
    border: solid 2px var(--primary);
    border-radius: 15px;
    padding: 2rem;
    display: flex;
    background-color: white;
}

.projectLeft{
    flex: 1;
}

.projectContainer .buttons{
    display: flex;
    flex-direction: column;
    gap: 1rem;
    justify-content: center;
    align-items: center;
}

.projectContainer .buttons *{
    padding: 0.5rem 1rem;
    width: 100%;
    border-radius: 15px;
    text-decoration: none;
    text-align: center;
    font-size: 1.25rem;
    color: white;
    background-color: var(--secondary);
}

#techStack{
    display: flex;
    gap: 1.5rem;
}

.techStackNode{
    background-color: var(--secondary);
    color: white;
    padding: 0.5rem 1rem;
    border-radius: 15px;
    font-size: 120%;
    width: 8%;
    text-align: center;
}

.projectContainer p{
    color: var(--tertiary);
}

.projectContainer h3{
    color: var(--secondary);
}

@media screen and (max-width: 800px){
    .projectContainer{
        flex-direction: column;
    }
}

</style>