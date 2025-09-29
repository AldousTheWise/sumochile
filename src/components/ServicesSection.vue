<template>
    <section class="relative bg-cover bg-center bg-no-repeat px-4 md:px-6 py-12 md:py-24 min-h-screen"
        style="background-image: url('/img/sumomeet.jpg');">

        <!-- Contenedor móvil (solo para mobile) -->
        <div class="md:hidden flex flex-col gap-8 pt-4 pb-8">
            <!-- 1. Sección ÚNETE -->
            <div class="bg-white/80 w-full p-6 text-center">
                <h2 class="text-red-600 font-anton text-4xl mb-2 font-bold">ÚNETE</h2>
                <p class="text-sm font-outfit text-black leading-relaxed">
                    ¡Acompáñamos a escribir esta historia!
                </p>
            </div>

            <!-- 2. Sección Clases -->
            <div class="bg-red-600/80 text-white p-5 w-full">
                <h1 class="text-3xl font-anton font-semibold">Clases Formativas</h1>
                <h3 class="text-xl font-anton text-black">Para todas las edades!</h3>
                <p class="font-outfit text-sm mt-2">
                    Mejora física, confianza y comunidad. ¡Solo necesitas ganas de aprender!
                </p>
            </div>

            <!-- 3. Sección Beneficios -->
            <div class="bg-red-600/80 text-white p-5 w-full">
                <h3 class="text-xl font-anton mb-2">Beneficios</h3>
                <ul class="font-outfit space-y-3 text-sm">
                    <li><span class="item-title">Defensa Personal: </span> Control de calma en situaciones de agresión.
                    </li>
                    <li><span class="item-title">Fuerza y agilidad: </span> Desarrollo físico integral.</li>
                    <li><span class="item-title">Equilibrio:</span> Mejora física y mental.</li>
                    <li><span class="item-title">Diversión: </span> Rompe con la rutina semanal.</li>
                </ul>
            </div>
        </div>

        <!-- Versión Desktop (original) -->
        <div class="hidden md:block">
            <!-- Headline -->
            <div class="absolute top-0 left-34 w-[80%] h-24 bg-white"></div>

            <!-- Sección ÚNETE -->
            <div class="absolute top-0 left-28 bg-white/80 w-90 p-10 text-center shape-flecha">
                <h2 class="text-red-600 font-anton text-8xl mb-4 font-bold">ÚNETE</h2>
                <p class="text-base font-outfit text-black leading-relaxed">
                    ¡Acompáñamos a escribir esta historia!
                </p>
            </div>

            <!-- Sección Clases -->
            <div class="curso bg-red-600/80 w-96 h-3/4 p-5 text-white absolute bottom-0 right-30">
                <h1 class="text-7xl font-anton font-semibold">Clases Formativas</h1>
                <h3 class="text-2xl font-anton text-black">Para todas las edades!</h3>
                <p class="font-outfit">Mejora física, confianza y comunidad. ¡Solo necesitas ganas de aprender!</p>
            </div>

            <!-- Sección Beneficios -->
            <div class="beneficios absolute bottom-0 left-34 bg-red-600/80 text-white p-5 w-1/2">
                <h3 class="text-2xl font-anton">Beneficios</h3>
                <ul class="font-outfit">
                    <li><span class="item-title">Defensa Personal: </span> Control de calma en situaciones de agresión.
                    </li>
                    <li><span class="item-title">Fuerza y agilidad: </span> Desarrollo físico integral.</li>
                    <li><span class="item-title">Equilibrio:</span> Mejora física y mental.</li>
                    <li><span class="item-title">Diversión: </span> Rompe con la rutina semanal.</li>
                </ul>
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

/* Estilos desktop */
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
    border-top: 50px solid rgba(255, 255, 255, 0.836);
}

.item-title {
    font-size: 1.5rem;
    font-weight: 600;
    font-family: "Anton", sans-serif;
    color: black;
}

/* Mobile específico */
@media (max-width: 767px) {
    .item-title {
        font-size: 1.1rem;
        display: inline-block;
        margin-right: 0.3rem;
    }
}
</style>