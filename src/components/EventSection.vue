<script setup>
import { ref } from 'vue';
import eventBgImg from '@/assets/img/sumito2.png';
import logoImg from '@/assets/img/sumo.png';

const eventos = ref([
    {
        id: 1,
        nombre: 'Campeonato Nacional',
        fecha: '15 de Junio'
    },
    {
        id: 2,
        nombre: 'Entrenamiento Abierto',
        fecha: '22 de junio'
    },
    {
        id: 1,
        nombre: 'Torneo Juvenil',
        fecha: '06 de Junio'
    },
    {
        id: 1,
        nombre: 'Exhibición Mall',
        fecha: '15 de Junio'
    }
]);
</script>

<template>
    <section class="relative flex flex-col justify-between bg-cover bg-center bg-no-repeat min-h-[100dvh]"
        :style="{ backgroundImage: `url( ${eventBgImg})` }">

        <div class="relative w-full">
            <div class="bg-white/80 w-2xl h-44 py-4 px-10 clip-diagonal-right">
                <h2 class="font-anton text-6xl text-red-600 font-bold leading-tight">
                    Próximos eventos y campeonatos.
                </h2>
            </div>

            <div class="absolute top-20 right-[40%] w-60 z-20">
                <img :src="logoImg" alt="Logo Sumo Chile" class="w-full">
            </div>
        </div>

        <div class="w-full flex justify-end px-40">
            <div id="base" class="font-outfit text-center">
                <h3 class="text-6xl font-anton text-red-600 my-8 uppercase font-bold">
                    Cartelera
                </h3>
                <ul class="text-xl leading-relaxed text-black mt-2.5 space-y-3">
                    <li v-for="evento in eventos" :key="evento.id">
                        <span class="font-semibold">{{ evento.nombre }}</span> - {{ evento.fecha }}
                    </li>
                </ul>
            </div>
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
    position: relative;
    width: 480px;
    min-height: 350px;
    background-color: white;
    padding: 2rem;
    z-index: 10;
}

#base:before {
    content: "";
    position: absolute;
    top: -40px;
    left: 0;
    transform: none;
    border-left: 240px solid transparent;
    border-right: 240px solid transparent;
    border-bottom: 40px solid white;
}
</style>