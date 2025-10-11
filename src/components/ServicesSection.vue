<script setup>
import serviceBgImg from '@/assets/img/sumomeet.jpg';
</script>

<template>
    <section class="relative bg-cover bg-center bg-no-repeat h-auto lg:min-h-[100dvh]"
        :style="{ backgroundImage: `url(${serviceBgImg})` }">
        <div class="hidden lg:block">
            <div class="absolute top-0 left-34 w-[78.1%] h-24 bg-white"></div>

            <div class="absolute top-0 left-28 bg-white w-90 p-10 text-center shape-flecha">
                <h2 class="text-red-600 font-anton text-8xl mb-4 font-bold">Únete.</h2>
                <p class="text-base font-outfit text-black leading-relaxed">
                    ¡Acompáñanos a escribir esta historia!
                </p>
            </div>
            <div class="curso bg-red-600/80 w-96 h-3/4 p-5 text-white absolute bottom-0 right-10">
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
        </div>
        <div class="lg:hidden flex flex-col items-center">
            <div class="bg-white w-10/12 h-25 p-6 text-center mb-10 self-start">
                <h2 class="text-red-600 font-anton text-5xl font-bold">ÚNETE</h2>
                <p class="text-sm font-outfit text-black leading-relaxed">
                    ¡Acompáñanos a escribir esta historia!
                </p>
            </div>

            <div class="w-full max-w-sm md:max-w-3xl flex flex-col md:flex-row gap-8 mx-10 mb-5">

                <div class="bg-red-600/80 text-white text-center p-3 w-full md:w-1/2 h-fit">
                    <h3 class="text-3xl font-anton font-semibold leading-relaxed"> Clases Formativas </h3>
                    <h4 class="text-xl font-anton text-black">Para todas las edades.</h4>
                    <p class="font-outfit text-sm mt-2">
                        Mejora física, confianza y comunidad. ¡Solo necesitas ganas de aprender!
                    </p>
                </div>

                <div class="bg-white/80 text-black p-5 w-full md:w-1/2">
                    <h3 class="text-3xl font-anton mb-2 text-red-600">Beneficios</h3>
                    <ul class="font-outfit space-y-3 text-sm">
                        <li><span class="item-title-mobile">Defensa Personal: </span> Control de calma en situaciones de
                            agresión.</li>
                        <li><span class="item-title-mobile">Fuerza y agilidad: </span> Desarrollo físico integral.</li>
                        <li><span class="item-title-mobile">Equilibrio:</span> Mejora física y mental.</li>
                        <li><span class="item-title-mobile">Diversión: </span> Rompe con la rutina semanal.</li>
                    </ul>
                </div>

            </div>
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