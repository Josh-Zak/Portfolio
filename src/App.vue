<script setup></script>

<template>
    <div class="main">
        <div id="header">
            <p class="name">Josh Zak&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;FullStack Engineer</p>
            <div id="nav">
                <a class="projects" href="#sec2">Projects</a>
                <a class="about" href="#sec3">About</a>
            </div>
        </div>
        <div id="sec1" class="section">
            <div id="sec1Left">
                <h1>Josh Zak</h1>
                <h2>Full-Stack Engineer</h2>
                <p>
                    I craft elegant solutions to complex problems using modern technologies.
                    Specializing in scalable applications and open-source contributions.
                </p>
                <div id="sec1Buttons">
                    <a class="linkedin" href="https://www.linkedin.com/in/joshzak19" target="_blank">
                        <GrommetIconsLinkedinOption id="linkedinIcon"/>
                        LinkedIn
                    </a>
                    <a class="github" href="https://github.com/Josh-Zak" target="_blank">
                        <GrommetIconsGithub id="githubIcon"/>
                        Github
                    </a>
                </div>
            </div>
            <div id="sec1Right">
                <img src="@/assets/headshot.jpg" alt="Profile" >
            </div>
        </div>
        <div id="sec2" class="section">
            <h2>My Work</h2>
            <p>Here's an overview of some of my work.</p>
            <div class="projects">
                <Project 
                    name="Cryptotrage"
                    desc="Full-stack crypto arbitrage platform aggregating real-time exchange data to identify profitable trading opportunities."
                    :stack="cryptoTrageTechStack"
                    link="dummy"
                    github="dummy"
                />
                <Project 
                    name="Proj2"
                    desc="blah blah blah"
                    link="dummy"
                    github="dummy"
                />
            </div>
        </div>
        <div id="sec3" class="section">
            <h2>About Me</h2>
            <div class="aboutDetails">
                <div class="professional">
                    <h3>Professional</h3>
                    <p>
                        Ever since I was young, I was always on the computer. From YouTube to
                        video games it's always been one of my favourite hobbies. In university,
                        I decided to pursue a degree in computer science where I discovered
                        software engineering and web developemnt. In my first position as a
                        Junior Software Developer at Wavelo, I got the opportunity to learn so
                        much working alongside senior developers. Today I'm currently working at
                        Miipe as a Quality Assurance Analyst where I'm learning about Software
                        Development from a testers perspective. It's really changed the way I
                        think about developemnt. I'm more aware of edge cases and deliverables as
                        they relate to business requirements.
                    </p>
                </div>
                <div class="personal">
                    <h3>Personal</h3>
                    <p>
                        I'm a "go all day" kind of person. I love my activities and sports. I play
                        hockey, I ski, mountain bike, hike, camp, snowmobile, dirt bike and ATV
                        just to name a few. I'm super competitive, and I'm always up for a good
                        challenge, which is probably why I also love board games. Catan anyone?
                        If I'm relaxing at home I like to play video games and watch movies. Some
                        of my favourite games include Battlefield, League of Legends, and Call of
                        Duty, while my favourite movies are Avatar, Star Wars (not the new ones),
                        and Batman. Here are some fun facts about me: I'm very fascinated by space
                        and I did an astronomy minor in university, I have a national bronze medal
                        from a ski competition from when I was 8, and my favourite band is Billy Talent
                        (big music guy too).
                    </p>
                </div>
            </div>
        </div>
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
    import GrommetIconsGithub from '~icons/grommet-icons/github'
    import GrommetIconsLinkedinOption from '~icons/grommet-icons/linkedin-option'
    export default{
        data() {
            return{
                year: new Date().getFullYear(),
                cryptoTrageTechStack: ["Vue.js", "Node.js"]
            }
        },
        components: {
            Project,
            GrommetIconsLinkedinOption,
            GrommetIconsGithub
        }
    }

</script>




<style>

.main{
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
}

#header{
    display: flex;
    justify-content: space-between;
    padding: 0 8rem;
    background-color: var(--primary);
}

#header .name{
    color: white;
}

#header .about{
    color: white;
}

#header .projects{
    color: white;
}

#nav{
    display: flex;
    gap: 5rem;
    align-items: center;
}

#nav a{
    text-decoration: none;
    font-size: 1.2rem;
}

.projects{
    display: flex;
    flex-direction: column;
    gap: 2rem;
}

#sec1 h1, #sec2 h2, #sec3 h2{
    color: var(--primary);
}

#sec1 h2{
    color: var(--secondary);
}

#sec1 #sec1Buttons{
    display: flex;
    gap: 3rem;
}

#sec1Buttons a{
    display: flex;
    align-items: center;
    justify-content: center;
}

#sec1 .linkedin, #sec1 .github{
    background-color: var(--primary);
    width: 24%;
}

#linkedinIcon, #githubIcon{
    stroke: white;
    color: transparent;
    height: 1.75rem;
    width: 1.75rem;
}

#sec1 a{
    border-radius: 5px;
    padding: 1rem 2rem;
    text-decoration: none;
    color: var(--primary);
    font-size: 1.5rem;
    gap: 1rem;
    color: white;
}

#sec1Left{
    width: 60%;
}

#sec1Right{
    display: flex;
    justify-content: center;
    align-items: center;
    width: 40%;
}

#sec1Right img{
    flex: 0 1 200px;
    height: 100%;
    border-radius: 50%;
    border: solid 2px var(--secondary);
    max-height: 400px;
}

p{
    color: var(--tertiary);
}

#sec2{
    background-color: rgb(243, 243, 243);
}

#sec3{
    display: flex;
    flex-direction: column;
}

#sec3 .professional, #sec3 .personal{
    color: var(--secondary);
    text-align: justify;
}

#sec1{
    display: flex;
    padding: 14rem 8rem;
}

#sec2, #sec3{
    padding: 6rem 8rem;
}

.aboutDetails{
    width: 100%;
    display: flex;
    gap: 2rem;
}

.aboutDetails > * {
    width: 50%;
    border: solid 2px var(--primary);
    background-color: rgb(243, 243, 243);
    border-radius: 1rem;
    padding: 1rem 2rem;
}

.footer{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 8rem;
    background-color: var(--primary);
}

.footer p{
    color: white;
}


</style>
