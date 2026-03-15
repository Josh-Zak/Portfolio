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
        <p>© {{ year }} Josh Zak</p>
        <div class="links">
            <button class="linkedinFooter">LinkedIn</button>
            <button class="githubfooter" >GitHub</button>
        </div>
    </div>
  </div>
</template>


<script>
    import Project from "@/Project.vue";
    export default{
        data() {
            return{
                year: new Date().getFullYear()
            }
        },
        components: {
            Project
        }
    }

</script>




<style>

.main{
    display: flex;
    flex-direction: column;
    gap: 3rem;
}

#header{
    display: flex;
    justify-content: space-between;
    padding: 0 4rem;
}

#header .name{
    color: var(--primary);
}

#header .about{
    color: var(--secondary);
}

#header .projects{
    color: var(--tertiary);
}

.nav{
    display: flex;
    gap: 2rem;
}

.projects{
    display: flex;
}

#sec1 h1, #sec2 h2, #sec3 h2{
    color: var(--primary);
}

#sec1 h2{
    color: var(--secondary);
}

p{
    color: var(--tertiary);
}

#sec3{
    display: flex;
    flex-direction: column;
}

#sec3 .professional, #sec3 .personal{
    color: var(--secondary);
}

#sec1, #sec2, #sec3{
    align-self: center;
    width: 70%;
}

.aboutDetails{
    width: 100%;
    display: flex;
}

.aboutDetails > * {
    width: 50%;
}

.footer{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 4rem;
}

h1{
    font-size: xxx-large;
}

h2{
    font-size: xx-large;
}

</style>
