<script setup>
import { ref } from 'vue'
import TimelineContentStart from './TimelineContentStart.vue';
const props = defineProps({
    studies: Array
})
</script>
<template>
    <ul class="timeline timeline-snap-icon max-md:timeline-compact timeline-vertical">
        <TimelineContentStart v-for="(studie, index) in studies" :what="studie.what" :where="studie.where"
            :when="studie.when" :timelength="studie.timelength" :about="studie.about" :index="index"
            :length="studies.length" />
    </ul>
</template>