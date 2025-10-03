<script setup>
import serviceBgImg from '@/assets/img/sumomeet.jpg';
</script>

<template>
    <section class="relative bg-cover bg-center bg-no-repeat min-h-[100dvh]"
        :style="{ backgroundImage: `url(${serviceBgImg})` }">

        <div class="absolute top-0 left-34 w-[78.1%] h-24 bg-white"></div>

        <div class="absolute top-0 left-28 bg-white w-90 p-10 text-center shape-flecha">
            <h2 class="text-red-600 font-anton text-8xl mb-4 font-bold">Únete.</h2>
            <p class="text-base font-outfit text-black leading-relaxed">
                ¡Acompáñanos a escribir esta historia!
            </p>
        </div>
        <div class="curso bg-red-600/80 w-96 h-3/4 p-5 text-white absolute bottom-0 right-20">
            <h3 class="text-7xl font-anton font-semibold ">
                Clases formativas.
            </h3>
            <h4 class="text-2xl font-anton text-black">
                Para todas las edades.
            </h4>
            <p class="font-outfit">Mejora física, confianza y comunidad. ¡Solo necesitas ganas de aprender!</p>
        </div>
        <div class="beneficios absolute bottom-0 left-34 bg-red-600/80 text-white p-5 w-1/2">
            <h3 class="text-6xl font-anton">Beneficios</h3>
            <ul class="font-outfit">
                <li><span class="item-title">Defensa Personal:</span> Aprende a mantener la calma en situaciones de
                    agresión.</li>
                <li><span class="item-title">Fuerza y Agilidad:</span> Desarrollo físico integral.</li>
                <li><span class="item-title">Equilibrio:</span> Mejora física y mental.</li>
                <li><span class="item-title">Diversión:</span> Rompe con la rutina semanal.</li>
            </ul>

        </div>
    </section>
</template>

<style scoped>
.font-anton {
    font-family: "Anton", sans-serif;
}

.font-outfit {
    font-family: "Outfit", sans-serif;
}

.shape-flecha {
    position: relative;
}

.shape-flecha::after {
    content: "";
    position: absolute;
    bottom: -50px;
    left: 50%;
    transform: translateX(-50%);
    width: 0;
    height: 0;
    border-left: 181px solid transparent;
    border-right: 181px solid transparent;
    border-top: 50px solid rgba(255, 255, 255 0.836);
}

.item-title {
    font-size: 1.5rem;
    font-weight: 600;
    font-family: 'Anton', sans-serif;
    color: black;
}
</style>