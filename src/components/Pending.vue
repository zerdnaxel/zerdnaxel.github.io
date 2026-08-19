<script setup>
import { ref } from 'vue'
import Hero from './Hero.vue';
// import ThemeCtlr from './ThemeCtlr.vue';
import StudiesTimeline from './Timeline/StudiesTimeline.vue';
import CV from '../data/CV.json';

const name = CV.first_name + " " + CV.last_name
const job_desc = CV.job

function getJobDesc() {
    var temp = "| "
    CV.job.forEach(job => {
        temp += job
        temp += " | "
    });
    return temp;
}

</script>

<template>
    <!-- <ThemeCtlr /> -->
    <Hero :title=name :description="getJobDesc()" />
    <StudiesTimeline :studies="CV.studies" />


</template>