<template>
    <div class="fixed inset-0 bg-slate-400 z-20">
        <div class="text-9xl flex items-center justify-center h-screen">
            {{ percentage }}%
        </div>
    </div>
</template>

<script lang="ts" setup>
const percentage = ref(0);

onMounted(() => {
    const tl = gsap.timeline();
    tl.to(percentage, {
        progress: 100,
        duration: 1,
        value: 25,
        ease: "power2.inOut",
        onUpdate() {
            percentage.value = Math.floor(percentage.progress);
        },
        onComplete() {
            general.isPreloaderVisible = false;
        },
    });
});
</script>

<style></style>
