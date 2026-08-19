<script setup>
const props = defineProps({
    when: String,
    where: String,
    what: String,
    timeLength: String,
    opposite: Boolean
})
</script>
<template>
    <li>
        <div class="timeline-middle">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="h-5 w-5">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.857-9.809a.75.75 0  "
                    clip-rule="evenodd" />
            </svg>
        </div>
        <div v-if=opposite class="timeline-end md:mb-10">
            <time class="font-mono italic">{{ when }}</time>
            <div class="text-lg font-black">{{ what }}</div>
            {{ where }}
        </div>
        <div v-else class="timeline-start mb-10 md:text-end">
            <time class="font-mono italic">{{ when }}</time>
            <div class="text-lg font-black">{{ what }}</div>
            {{ where }}
        </div>
        <hr />
    </li>
</template>