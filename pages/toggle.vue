<template>
    <section class="container mx-auto max-w-4xl flex flex-col gap-4 py-20 px-6">
        <h1 class="text-6xl mb-4">Toggle</h1>
        <div>
            <button @click="toggle">Toggle Sichtbarkeit</button>
            <transition
                @before-enter="beforeEnter"
                @enter="enter"
                @after-enter="afterEnter"
                @before-leave="beforeLeave"
                @leave="leave"
                @after-leave="afterLeave"
            >
                <p v-if="visible">
                    Dieses Element wird ein- und ausgeblendet. Lorem ipsum dolor
                    sit amet consectetur adipisicing elit. Obcaecati, quis
                    deleniti dicta animi, distinctio officia perspiciatis magnam
                    ipsam totam modi nesciunt, aspernatur assumenda dolores
                    consectetur.
                </p>
            </transition>
        </div>
    </section>
</template>

<script setup lang="ts">
const visible = ref(false);

function toggle() {
    visible.value = !visible.value;
}

function beforeEnter(el) {
    console.log("Vor dem Eintritt");
}

function enter(el, done) {
    console.log("Eintritt");
    // Beispiel für eine asynchrone Operation
    setTimeout(() => {
        done();
    }, 1000);
}

function afterEnter(el) {
    console.log("Nach dem Eintritt");
}

function beforeLeave(el) {
    console.log("Vor dem Verlassen");
}

function leave(el, done) {
    console.log("Verlassen");
    setTimeout(() => {
        done();
    }, 1000);
}

function afterLeave(el) {
    console.log("Nach dem Verlassen");
}
</script>

<style>
.fade-enter-active,
.fade-leave-active {
    transition: all 1.4s;
}
.fade-enter-from,
.fade-leave-to {
    opacity: 0;
}
</style>
