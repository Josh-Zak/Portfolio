<script setup></script>

<template>
  <div class="main">
    <div id="header">
        <div class="name">Josh Zak - FullStack Engineer</div>
        <div class="nav">
            <div class="about">About</div>
            <div class="projects">Projects</div>
        </div>
    </div>
    <hr>
    <div id="sec1" class="section">
        <h1>Josh Zak</h1>
        <h2>Full-Stack Engineer</h2>
        <p>
            I craft elegant solutions to complex problems using modern technologies.
            Specializing in scalable applications and open-source contributions.
        </p>
        <div class="buttons">
            <button class="linkedin">LinkedIn</button>
            <button class="github">GitHub</button>
        </div>
    </div>
    <hr>
    <div id="sec2" class="section">
        <h2>My Work</h2>
        <p>Here's an overview of some of my work.</p>
        <div class="projects">
            <Project name="Cryptotrage" desc="blah blah blah" link="dummy" github="dummy"/>
            <Project name="Proj2" desc="blah blah blah" link="dummy" github="dummy"/>
        </div>
    </div>
    <hr>
    <div id="sec3" class="section">
        <h2>About Me</h2>
        <div class="aboutDetails">
            <div class="professional">
                <h3>Professional</h3>
                <p>Learn more about my background and experience.</p>
            </div>
            <div class="personal">
                <h3>Personal</h3>
                <p>Discover my interests and hobbies outside of work.</p>
            </div>
        </div>
    </div>
    <hr>
    <div class="footer">

    </div>
  </div>
</template>


<script>
    import Project from "@/Project.vue";


    export default{
        components: {
            Project
        }
    }



</script>




<style>

/* 
Background White
Primary 214687
Secondary 83ABE4
Tertiary4688E0
*/

*,
*::before,
*::after {
    box-sizing: border-box;
}


.main{
    display: flex;
    flex-direction: column;
}

.main > *{
    border: solid black;
}

#header{
    display: flex;
    justify-content: space-between;
    padding: 0 1rem;
}

.nav{
    display: flex;
    gap: 2rem;
}

.projects{
    display: flex;
}

#sec3{
    display: flex;
    flex-direction: column;
}

.aboutDetails{
    display: flex;
}

</style>
