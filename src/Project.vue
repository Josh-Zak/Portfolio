<template>
    <div class="projectContainer">
        <h3>{{ name }}</h3>
        <p>{{ desc }}</p>
        <div class="buttons">
            <button class="link">Link</button>
            <button class="github">GitHub</button>
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
        github: String
    }
}
</script>


<style>
.projectContainer{
    border: solid black;

}
</style>