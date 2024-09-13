<template>
    <div>
        <Preloader />
        <main>
            <pre>default layout</pre>
            <slot />
        </main>
    </div>
</template>

<script lang="ts" setup>
import Preloader from "~/components/preloader.vue";
</script>

<style scoped>
div {
    background-color: lightgreen;
}
</style>
