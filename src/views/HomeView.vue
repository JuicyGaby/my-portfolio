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

        <div class="skills pa-5 d-flex flex-column justify-center align-center" id="skills">
            
            <div class="mb-5">
                <h2 class="">Utilized Technologies</h2>
                <hr>
            </div>
            <v-container class="fluid" >
                <v-row class="mb-9">
                    <v-col class="cards">
                        <v-tooltip 
                        activator="parent"
                        location="bottom"
                        >
                        HTML5
                        </v-tooltip>
                        <!-- <v-icon class="text-h1" @mouseover="handleCards('html')" @mouseout="data.skills.isHovered = false" id="html">mdi-language-html5</v-icon> -->
                        <v-icon class="text-h1" color="#F46527">mdi-language-html5</v-icon>
                    </v-col>
                    <v-col class="cards" width="">
                        <v-tooltip 
                        activator="parent"
                        location="bottom"
                        >
                        CSS3
                        </v-tooltip>
                        <v-icon class="text-h1" color="#0E70B8">mdi-language-css3</v-icon>
                    </v-col>
                    <v-col class="cards">
                        <v-tooltip 
                        activator="parent"
                        location="bottom"
                        >
                        JAVASCRIPT
                        </v-tooltip>
                        <v-icon class="text-h1" color="#E7A829">mdi-language-javascript</v-icon>
                    </v-col>
                    <v-col class="cards">
                        <v-tooltip 
                        activator="parent"
                        location="bottom"
                        >
                        VUE3 JS
                        </v-tooltip>
                        <v-icon class="text-h1" color="#3FB984">mdi-vuejs</v-icon>
                    </v-col>
                </v-row>
                <v-row>
                    <v-col class="cards">
                        <v-tooltip 
                        activator="parent"
                        location="bottom"
                        >
                        NODE JS
                        </v-tooltip>
                        <v-icon class="text-h1" color="#90C53F">mdi-nodejs</v-icon>
                    </v-col>
                    <v-col class="cards">
                        <v-tooltip 
                        activator="parent"
                        location="bottom"
                        >
                        PYTHON
                        </v-tooltip>
                        <v-icon class="text-h1" color="#2D6B9B">mdi-language-python</v-icon>
                    </v-col>
                    <v-col class="cards">
                        <v-tooltip 
                        activator="parent"
                        location="bottom"
                        >
                        BOOTSTRAP
                        </v-tooltip>
                        <v-icon class="text-h1" color="#7D0AF8">mdi-bootstrap</v-icon>
                    </v-col>
                    <v-col class="cards">
                        <v-tooltip 
                        activator="parent"
                        location="bottom"
                        >
                        GIT
                        </v-tooltip>
                        <v-icon class="text-h1" color="#F05033">mdi-git</v-icon>
                    </v-col>
                </v-row>
            </v-container>
        </div>
        <div class="projects d-flex justify-center align-center flex-column" id="projects">
            <div class="">
                <h2>Projects Developed</h2>
                <hr>
            </div>
            <v-container grid-list-xs>
                
            </v-container>
        </div>
        <!-- <BackToTopBtn /> -->
        <footer id="contact">
            <v-footer
            color="#FF8303"
            class="
            text-center
            d-flex
            flex-column
            "
            >   
                <div class="">
                    <v-btn
                    v-for="icon in icons"
                    :key="icon"
                    class="mx-4"
                    :icon="icon"
                    variant="text"
                    ></v-btn>
                </div>
                <v-divider></v-divider>
                <div class="">
                    2023 - Gabe Fletcher Sanchez
                </div>
            </v-footer>
        </footer>
    </div>
    
</template>
<script>

// importing vue components
import BackToTopBtn from '../components/BackToTopBtn.vue'

export default {
    components: {
        BackToTopBtn,
    },
    data() {
        return {
            data: {
                skills: {
                    isHovered: false,
                }
            },
            icons: [
                'mdi-facebook',
                'mdi-twitter',
                'mdi-instagram',
                'mdi-linkedin',
                'mdi-github',
            ]
        }
    },
    methods: {
        scrollToElement(elementId) {
            const destination = document.querySelector(elementId)
            window.scrollTo({
                behavior: 'smooth',
                top: destination.offsetTop
            })
        },
    },
}
</script>
<style lang="css" scoped>
.root {
    --border: 1px red dashed;
    --darkBg: #1B1A17;
    --lightBg: #242320;
    --textColor: #F0E3CA;
    --accent: #FF8303;
    --accent2: #A35709;
}

* {
    /* border: var(--border); */
}

html {
    scroll-behavior: smooth;
}

hr {
    border-color: var(--accent);
    height: 4px;
    background-color: var(--accent);
}
h2 {
    color: var(--accent);
}

/* main starts */


.logo {
    color: var(--accent);
}

.topBtn {
    position: fixed;
    bottom: 8%;
    right: 5%;
    z-index: 100;
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
    background-color: var(--darkBg);
}

.cards {
    background: var(--lightBg);
    border-radius: 5px;
    display: flex;
    align-items: center;
    justify-content: center;
    /* padding: 3em; */
    margin: .5em;
    box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
}

/* skills ends */
.projects {
    height: 100vh;
    width: 100%;
    background-color: var(--lightBg);
}

.footer {
    height: 20vh;
    width: 100%;
    background-color: var(--darkBg);
}
</style>