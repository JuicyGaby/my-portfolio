<template lang="">
    <div class="main" id="about">
        <div class="navbar d-flex justify-space-between align-center py-2 px-3">
            <div class="">JuicyGaby</div>
            <div class="anchor">
                <ul class="d-inline-flex no-text-decoration">
                    <li><a @click="scrollToElement('#about')">About Me</a></li>
                    <li><a @click="scrollToElement('#skills')">Skills</a></li>
                    <li><a @click="scrollToElement('#projects')">Projects</a></li>
                    <li><a @click="scrollToElement('#contact')">Contact</a></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="description" id="">

    </div>
    <div class="skills" id="skills">

    </div>
    <div class="projects" id="projects">

    </div>
    <div class="footer" id="contact">

    </div>
</template>
<script>

export default {
    data() {
        return {
            
        }
    },
    methods: {
        scrollToElement(elementId) {
            const destination = document.querySelector(elementId)
            window.scrollTo({
                behavior: 'smooth',
                top: destination.offsetTop
            })
        }
    },
}
</script>
<style lang="css" scoped>
    /* main starts */
    html {
        scroll-behavior: smooth;
    }
    .main {
        height: 70vh;
        width: 100%;
        background-color: lightblue;
        border: 1px solid black;
    }
    div {
        border: 1px solid black;
    }
    ul li {
        list-style: none;
        margin-left: 10em;
        
    }
    a {
        text-decoration: none;
        cursor: pointer;
    }
    .navbar {
        height: 10%;
        border: 1px solid black;
    }

    /* main ends */
    .description {
        height: 30vh;
        width: 100%;
        background-color: lightgreen;
    }
    .skills {
        height: 100vh;
        width: 100%;
        background-color: lightblue;
    }
    .projects {
        height: 100vh;
        width: 100%;
        background-color: lightgreen;
    }
    .footer {
        height: 20vh;
        width: 100%;
        background-color: lightblue;
    }
</style>