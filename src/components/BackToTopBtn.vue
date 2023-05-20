<template lang="">
    <transition name="fade">
        <v-btn
        v-if="showButton"
        color="#FF8303"
        size="large"
        icon="mdi-chevron-up"
        class="back-to-top-button"
        @click="scrollToTop"
        >
        </v-btn>
    </transition>
</template>
<script>
export default {
    data() {
        return {
            showButton: false,
        }
    },
    mounted() {
        window.addEventListener('scroll', this.handleScroll);
    },
    beforeDestroy() {
        window.removeEventListener('scroll', this.handleScroll);
    },
    methods: {
        handleScroll() {
            this.showButton = window.pageYOffset > 200
        },
        scrollToTop() {
            console.log('sdfds');
            window.scrollTo({top : 0, behavior : 'smooth'})
        }
    },
}
</script>

<style>

.fade-enter-active,
.fade-leave-active {
  transition: opacity 3s;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>