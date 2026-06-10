<script>
import Hero from './Hero.vue';
import ThemeCtlr from './ThemeCtlr.vue';
export default {
    data() {
        return {
            btnContent: 'Button'
        }
    },
    methods: {
        ChangeButton() {
            this.btnContent = "(not a) Button";
        }
    }
}
</script>

<template>
    <Hero />
    <h1>Welcome</h1>
    <h2>we are not here yet</h2>
    <p>this website is not finished yet, please wait!!!</p>
    <button class="btn btn-primary" @click="ChangeButton">{{ btnContent }}</button>

</template>