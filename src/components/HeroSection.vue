<script setup>
import carouselImage from '@/assets/img/carousel2.jpg';
import logoSumo from '@/assets/img/sumo.png';

const bienvenida = "Bienvenido a Sumo Chile.";
const texto = "Federación Chilena de Sumo.";
</script>

<template>
    <section class="relative h-[100dvh] overflow-hidden">
        <!-- Fondo (visible en ambas versiones) -->
        <div class="absolute inset-0 z-0">
            <img :src="carouselImage" alt="Foto Sumo" class="w-full h-full object-cover" />
        </div>

        <!-- Banda roja diagonal (solo desktop) -->
        <div class="hidden md:block absolute top-0 left-0 w-3/5 h-32 bg-red-600/90 z-100 clip-diagonal-right shadow-xl">
        </div>

        <!-- Contenido principal -->
        <!-- Versión Desktop -->
        <div
            class="hidden md:flex absolute right-0 h-full w-1/2 lg:w-3/5 bg-white/80 z-10 clip-trapezoid shadow-2xl items-center justify-center px-6 md:px-8 lg:px-12">
            <div class="text-left md:p-8 w-full max-w-xl z-10 space-y-4">
                <h1
                    class="titulo text-4xl md:text-5xl lg:text-7xl xl:text-8xl text-red-600 font-bold break-words leading-tight">
                    {{ bienvenida }}
                </h1>
                <p class="texto text-lg md:text-2xl lg:text-3xl text-black">{{ texto }}</p>
            </div>
            <div class="logo absolute bottom-3 right-5 md:w-48 lg:w-60 z-0">
                <img :src="logoSumo" alt="Logo Sumo" class="w-full h-auto" />
            </div>
        </div>


    </section>
</template>

<style scoped>
.titulo {
    font-family: "Anton", sans-serif;
}

.texto {
    font-family: "Outfit", sans-serif;
}

.clip-trapezoid {
    clip-path: polygon(15% 0, 100% 0, 85% 100%, 0 100%);
}

.clip-diagonal-right {
    clip-path: polygon(0 0, 100% 0, 96.5% 100%, 0 100%);
}
</style>