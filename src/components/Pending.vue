<script>

import { ref } from 'vue'
import Hero from './Hero.vue';
import ThemeCtlr from './ThemeCtlr.vue';
export default {
    data() {
        return {
            btnContent: 'Button'
        }
    },
    components: {
        Hero
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

</template>