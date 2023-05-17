<template lang="">
    <div class="topBtn">
        <BackToTopBtn />
    </div>

    <div class="main" id="about">
        <v-toolbar color="primary" class="px-10">
            <v-toolbar-title>
                JuicyGaby
            </v-toolbar-title>
            <ul class="d-inline-flex no-text-decoration">
                <li><a @click="scrollToElement('#about')">About Me</a></li>
                <li><a @click="scrollToElement('#skills')">Skills</a></li>
                <li><a @click="scrollToElement('#projects')">Projects</a></li>
                <li><a @click="scrollToElement('#contact')">Contact</a></li>
            </ul>
        </v-toolbar>
        
    </div>
    <div class="description d-flex flex-column justify-center align-center" id="">
        <h2 class="mb-3">About Me</h2>
        <div class="d-flex justify-space-between align-center">
    
            <v-icon icon="mdi-information" class="mr-5" size="x-large"></v-icon>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.
                 Vitae deserunt <br> laudantium odit quo temporibus soluta qui
                  commodi modi veritatis ducimus.</p>
        </div>
        
        
    </div>
    <div class="skills" id="skills">

    </div>
    <div class="projects" id="projects">
    </div>
    <!-- <BackToTopBtn /> -->
    <div class="footer" id="contact">
    </div>
</template>
<script>

// importing vue components
import BackToTopBtn from '../components/BackToTopBtn.vue'

export default {
    components : {
      BackToTopBtn,
    },
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

.topBtn {
    position: fixed;
    bottom: 8%;
    right: 5%;
}
.main {
    height: 80vh;
    width: 100%;
    background-color: lightblue;
    border: 1px solid black;
}


ul li {
    list-style: none;
    margin-left: 5rem
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
    height: 20vh;
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