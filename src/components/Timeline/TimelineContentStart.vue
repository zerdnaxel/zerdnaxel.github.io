<script setup>
const props = defineProps({
    when: String,
    where: String,
    what: String,
    timelength: String,
    about: String,
    index: Number,
    length: Number
})
</script>
<template>
    <li v-if="index < length - 1">
        <div class="timeline-middle">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="h-5 w-5">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0"
                    clip-rule="evenodd" />
            </svg>
        </div>
        <div v-if="index % 2 == 1" class="timeline-end md:mb-10">
            <time class="font-mono italic">{{ when }} ({{ timeLenght }})</time>
            <div class="text-lg font-black">{{ what }}</div>
            {{ where }}
            <div v-if="about != null">{{ about }}</div>
        </div>
        <div v-else class="timeline-start mb-10 md:text-end">
            <time class="font-mono italic">{{ when }} ({{ timeLenght }})</time>
            <div class="text-lg font-black">{{ what }}</div>
            {{ where }}
            <div v-if="about != null">{{ about }}</div>
        </div>
        <hr />
    </li>
    <li v-else>
        <hr />
        <div class="timeline-middle">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="h-5 w-5">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0"
                    clip-rule="evenodd" />
            </svg>
        </div>
        <div v-if="index % 2 == 1" class="timeline-end md:mb-10">
            <time class="font-mono italic">{{ when }}</time>
            <div class="text-lg font-black">{{ what }}</div>
            {{ where }}
        </div>
        <div v-else class="timeline-start mb-10 md:text-end">
            <time class="font-mono italic">{{ when }}</time>
            <div class="text-lg font-black">{{ what }}</div>
            {{ where }}
        </div>
    </li>
</template>