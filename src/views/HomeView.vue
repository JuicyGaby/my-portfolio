<template lang="">
    <div class="root">
        <div class="topBtn">
            <BackToTopBtn />
        </div>

        <div class="main" id="about">
            <v-toolbar color="#1B1A17" class="px-10">
                <v-toolbar-title>
                    <span class="logo">JuicyGaby</span>
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
        <div class="skills pa-5 d-flex justify-center align-center" id="skills">
            <v-container class="">
                <v-row
                align-content="center"
                >
                    <v-col class="d-flex justify-center align-center">
                        <h2 class="mx-1">Utilized Technologies</h2>
                        <v-icon class="mx-1 text-h4">mdi-cogs</v-icon>
                    </v-col>
                </v-row>
                <v-row>
                    <v-col class="cards">
                            <v-icon class="text-h1">mdi-language-html5</v-icon>
                    </v-col>
                    <v-col class="cards">
                            <v-icon class="text-h1">mdi-language-css3</v-icon>
                    </v-col>
                    <v-col class="cards">
                            <v-icon class="text-h1">mdi-language-javascript</v-icon>
                    </v-col>
                    <v-col class="cards">
                            <v-icon class="text-h1">mdi-vuejs</v-icon>
                    </v-col>
                    <v-col class="cards">
                            <v-icon class="text-h1">mdi-nodejs</v-icon>
                    </v-col>
                    <v-col class="cards">
                            <v-icon class="text-h1">mdi-language-python</v-icon>
                    </v-col>
                    <v-col class="cards">
                            <v-icon class="text-h1">mdi-bootstrap</v-icon>
                    </v-col>
                    <v-col class="cards">
                            <v-icon class="text-h1">mdi-git</v-icon>
                    </v-col>
                </v-row>
            </v-container>
        </div>
        <div class="projects" id="projects">
        </div>
        <!-- <BackToTopBtn /> -->
        <div class="footer" id="contact">
        </div>
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
.root {
    --border : 1px red dashed;
    --darkBg : #1B1A17;
    --lightBg : #242320;
    --textColor: #F0E3CA;
    --accent: #FF8303;
    --accent2: #A35709;
}
* {
    border: var(--border);
}

html {
    scroll-behavior: smooth;
}
/* main starts */


.logo {
    color: var(--accent);
}
.topBtn {
    position: fixed;
    bottom: 8%;
    right: 5%;
}
.main {
    height: 80vh;
    width: 100%;
    background-color: var(--lightBg);
    /* border: var(--border); */
}

ul li {
    list-style: none;
    margin-left: 5rem
}

ul li a {
    text-decoration: none;
    cursor: pointer;
    color: var(--textColor);
    transition: all .5s;
}
ul li a:hover {
    color: var(--accent);
}

.navbar {
    height: 10%;
    border: 1px solid black;
}
/* main ends */
/* description starts */
.description {
    height: 20vh;
    width: 100%;
    background-color: var(--darkBg);

}
.description p {
    color: var(--textColor);
}
.description h2 {
    color: var(--accent);
}
/* description end */
/* skills starts */

.skills {
    height: 100vh;
    width: 100%;
    background-color: var(--lightBg);
}
.cards {
    background: var(--darkBg);
    display: flex;
    align-items: center;
    justify-content: center;
}
.cards span {
    height: 4rem;
}
/* skills ends */
.projects {
    height: 100vh;
    width: 100%;
    background-color: var(--darkBg);
}

.footer {
    height: 20vh;
    width: 100%;
    background-color: var(--lightBg);
}
</style>