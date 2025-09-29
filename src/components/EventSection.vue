<template>
    <section class="relative bg-cover bg-center bg-no-repeat px-4 md:px-6 py-12 md:py-24 min-h-screen"
        style="background-image: url('/img/sumito2.png');">

        <!-- Encabezado diagonal -->
        <div
            class="absolute top-0 left-0 bg-white/80 w-full md:w-2xl h-28 md:h-45 pl-4 md:pl-5 pt-4 md:pt-5 clip-diagonal-right">
            <h1 class="font-anton text-2xl md:text-6xl text-red-600 font-bold leading-tight">
                Próximos eventos y campeonatos
            </h1>
        </div>

        <!-- Logo (solo visible en desktop) -->
        <div class="hidden md:block absolute top-15 left-140 w-60 z-20">
            <img src="/img/sumo.png" alt="Logo Sumo Chile" class="w-full">
        </div>

        <!-- Cartelera -->
        <div id="base" class="font-outfit text-center">
            <h2 class="text-3xl md:text-6xl font-anton text-red-600 my-4 md:my-8 uppercase font-bold">Cartelera</h2>
            <ul class="text-base md:text-xl leading-relaxed text-black mt-2 md:mt-2.5 space-y-2 md:space-y-3">
                <li>Campeonato Nacional – 15 Junio</li>
                <li>Entrenamiento Abierto – 22 Junio</li>
                <li>Torneo Juvenil – 6 Julio</li>
                <li>Exhibición Internacional – 20 Julio</li>
            </ul>
        </div>
    </section>
</template>

<style scoped>
.clip-diagonal-right {
    clip-path: polygon(0 0, 100% 0, 96.5% 100%, 0 100%);
}

.font-anton {
    font-family: "Anton", sans-serif;
}

.font-outfit {
    font-family: "Outfit", sans-serif;
}

#base {
    position: absolute;
    bottom: 2rem;
    right: 5%;
    left: 5%;
    width: auto;
    max-width: 480px;
    height: auto;
    min-height: 300px;
    background-color: white;
    padding: 1.5rem;
    z-index: 10;
    margin: 0 auto;
}

#base:before {
    content: "";
    position: absolute;
    top: -20px;
    left: 50%;
    transform: translateX(-50%);
    width: 0;
    height: 0;
    border-left: 20px solid transparent;
    border-right: 20px solid transparent;
    border-bottom: 20px solid white;
}

/* Desktop específico */
@media (min-width: 768px) {
    #base {
        right: 10%;
        left: auto;
        width: 480px;
        height: 400px;
        padding: 2rem;
    }

    #base:before {
        top: -40px;
        left: 0;
        transform: none;
        border-left: 240px solid transparent;
        border-right: 240px solid transparent;
        border-bottom: 40px solid white;
    }
}

/* Ajustes para móviles pequeños */
@media (max-width: 400px) {
    #base {
        bottom: 1rem;
        padding: 1rem;
    }

    h1.font-anton {
        font-size: 1.5rem;
    }

    #base h2 {
        font-size: 2rem;
    }
}
</style>