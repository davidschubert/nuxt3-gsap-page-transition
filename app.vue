<template>
    <div class="bg-lime-400 min-h-screen">
        <NuxtRouteAnnouncer />
        <NuxtLoadingIndicator />
        <PageNavigation />
        <NuxtLayout>
            <NuxtPage />
        </NuxtLayout>
    </div>
</template>

<style>
.page-enter-active,
.page-leave-active {
    transition: all 1.4s;
}
.page-enter-from,
.page-leave-to {
    opacity: 0;
    filter: blur(1rem);
}

.layout-enter-active,
.layout-leave-active {
    transition: all 1.4s;
}
.layout-enter-from,
.layout-leave-to {
    transform: translateY(80px);
}

.rotate-enter-active,
.rotate-leave-active {
    transition: all 1.4s;
}
.rotate-enter-from {
    opacity: 0;
    transform: translateY(80px);
    transition-timing-function: cubic-bezier(0.42, 0, 0.58, 1);
}
.rotate-leave-to {
    opacity: 0;
}
</style>
