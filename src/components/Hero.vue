<script setup>
const props = defineProps({
    title: String,
    description: String
})
</script>
<template>
    <div className="hero bg-base-200 min-h-screen">
        <div className="hero-content flex-col lg:flex-row">
            <img src="https://img.daisyui.com/images/stock/photo-1635805737707-575885ab0820.webp"
                className="max-w-sm rounded-lg shadow-2xl" />
            <div>
                <h1 className="text-5xl font-bold">{{ title }}</h1>
                <p className="py-6">
                    {{ description }}
                </p>
            </div>
        </div>
    </div>
</template>