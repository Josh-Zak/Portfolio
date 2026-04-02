<script setup></script>

<template>
    <div class="main">
        <div id="header">
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
                    I build scalable and robust applications focused on solving real-world problems.
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
            </div>
        </div>
        <div id="sec3" class="section">
            <h2>About Me</h2>
            <div class="aboutDetails">
                <div class="professional">
                    <h3>Professional</h3>
                    <p>
                        I've always been drawn to computers, spending much of my time growing up playing
                        games, watching videos, and browsing the internet. This interest led me to pursue
                        a degree in Computer Science, where I discovered a passion for software
                        engineering and web development.
                    </p>
                    <p>
                        As a Software Developer at Wavelo, I had the opportunity to work alongside senior
                        engineers, gaining hands-on experience building and integrating real-world systems.
                        Today, as a Quality Assurance Engineer at Miipe, I approach development from a
                        tester's perspective—focusing on system behavior, edge cases, and alignment with
                        business requirements.
                    </p>
                    <p>
                        This unique perspective has strengthened my ability to think critically about
                        software design and development, helping me build more reliable and well-rounded
                        solutions.
                    </p>
                </div>
                <div class="personal">
                    <h3>Personal</h3>
                    <p>
                        I'm a "go all day" kind of person who loves staying active. I enjoy a wide range
                        of sports and outdoor activities, including hockey, skiing, mountain biking,
                        hiking, camping, and motorsports. I'm super competitive and always up for a
                        challenge, whether it's on the ice, on the trails, or around a board game (Catan,
                        anyone?).
                    </p>
                    <p>
                        When I'm relaxing, I like playing video games and watching movies. Some of my
                        favorites include Battlefield, League of Legends, and Call of Duty, along with
                        films like Avatar, Star Wars, and Batman.
                    </p>
                    <p>     
                        A few fun facts about me: I have a strong interest in space and completed a
                        minor in astronomy, earned a national bronze medal in the NASTAR ski racing
                        series, and my favorite genre of music is alternative rock.
                    </p>
                </div>
            </div>
        </div>
        <div id="footer">
            <p>© {{ year }} Josh Zak</p>
            <div class="links">
                <a class="linkedin" href="https://www.linkedin.com/in/joshzak19" target="_blank">
                    <GrommetIconsLinkedinOption id="linkedinIcon"/>
                </a>
                <a class="github" href="https://github.com/Josh-Zak" target="_blank">
                    <GrommetIconsGithub id="githubIcon"/>
                </a>
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
/* 2 things are class=project */
/* headshot still too big */
/* sec1 buttons shrink with screen size */


.main{
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
}



/* Header */
#header{
    display: flex;
    justify-content: center;
    padding: 0 10rem;
    background-color: var(--primary);
}

#header .about, #header .projects{
    color: white;
    margin: 1.5rem 0;
    font-size: 1.5rem;
    text-decoration: none;
}

#nav{
    display: flex;
    gap: 6rem;
    align-items: center;
}



/* Multiple secs */
#sec1 h1, #sec2 h2, #sec3 h2{
    color: var(--primary);
}

#sec2, #sec3{
    padding: 6rem 10rem;
}



/* Sec 1 */
#sec1 h2{
    color: var(--secondary);
}

#sec1{
    display: flex;
    padding: 14rem 10rem;
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
    display: flex;
    flex-direction: column;
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

@media screen and (max-width: 800px) {
    #sec1{
        flex-direction: column;
        padding: 4rem 2rem 6rem 2rem;
    }

    #sec1Left, #sec1Right{
        width: 100%;
    }

    #sec1Left{
        padding-bottom: 2rem;
        order: 1;
        text-align: center;
        align-items: center;
    }

    #sec1Right{
        order: 0;
    }

    #sec1Buttons{
        justify-content: center;
    }
}



/* Sec 2 */
.projects{
    display: flex;
    flex-direction: column;
    gap: 2rem;
}

#sec2{
    background-color: rgb(243, 243, 243);
}

@media screen and (max-width: 800px) {
    #sec2{
        padding: 6rem 2rem;
    }
}


/* Sec 3 */
#sec3{
    display: flex;
    flex-direction: column;
}

#sec3 .professional, #sec3 .personal{
    color: var(--secondary);
    text-align: justify;
}

.aboutDetails{
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    gap: 4rem;
    justify-content: center;
}

.aboutDetails > * {
    flex: 0 0 45%;
    border: solid 2px var(--primary);
    background-color: rgb(243, 243, 243);
    border-radius: 1rem;
    padding: 1rem 2rem;
    min-width: 600px;
}

@media screen and (max-width: 800px){
    #sec3{
        padding: 6rem 2rem;
    }

    .professional, .personal{
        width: 100%;
    }

    #sec3 p{
        font-size: 120%;
    }

    .aboutDetails{
        flex-direction: column;
    }
}



/* Footer */
#footer{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 10rem;
    background-color: var(--primary);
}

#footer p{
    color: white;
}

#footer .links{
    display: flex;
    gap: 2rem;
}

@media screen and (max-width: 800px) {
    #footer{
        padding: 0 2rem;
    }
}

</style>
