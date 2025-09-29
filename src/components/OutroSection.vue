<template>
    <section class="relative w-screen h-screen bg-red-600 overflow-hidden">
        <!-- Texto de fondo tipo patrón -->
        <div
            class="absolute inset-0 z-10 grid grid-cols-4 gap-0 text-white opacity-10 font-anton text-[6vw] leading-none place-items-center">
            <div v-for="n in 32" :key="n" class="whitespace-nowrap">
                SUMOCHILE
            </div>
        </div>

        <!-- Imagen central encima -->
        <div class="absolute inset-0 z-20 flex items-center justify-center pointer-events-none">
            <img src="/img/team2.jpg" alt="Nuestro Equipo" class="w-1/2 max-w-full max-h-full object-contain" />
        </div>
    </section>
</template>

<style scoped>
.font-anton {
    font-family: "Anton", sans-serif;
}
</style>
