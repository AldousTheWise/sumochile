<script setup>
import contactBgImg from '@/assets/img/wrestler.png';
</script>

<template>
    <section class="relative bg-cover bg-center bg-no-repeat lg:px-6  lg:min-h-[100dvh]"
        :style="{ backgroundImage: `url(${contactBgImg})` }">
        <div class="hidden lg:block">
            <div
                class="absolute w-[60%] h-[140px] top-0 right-0 bg-red-600 clip-diagonal-first-block z-10 flex items-center justify-center shadow-xl">
                <h2 class="text-white text-7xl font-semibold font-anton leading-relaxed">CONTÁCTANOS</h2>
            </div>

            <div class="relative z-20 mt-15 max-w-[100dvw] mx-auto h-[600px]">

                <div class="absolute top-0 left-0 bg-white/80 p-6 w-[45%] shadow-lg clip-diagonal-top-right">
                    <h3 class="text-2xl text-red-600 font-bold font-anton mb-2">ESCRÍBENOS</h3>
                    <p class="font-outfit text-lg mb-2">
                        ¿Tienes dudas? ¿Quieres sumarte? <br> ¡Mándanos tu mensaje!
                    </p>
                    <ul class="font-outfit text-base space-y-1 mt-4">
                        <li><strong>Email: </strong> contacto@sumochile.cl</li>
                        <li><strong>Instagram: </strong>@sumochile</li>
                        <li><strong>Facebook: </strong>Federación Chilena de Sumo.</li>
                        <li><strong>Tiktok: </strong>@sumochile</li>
                    </ul>
                </div>

                <div class="absolute bottom-0 right-0 bg-white/80 p-6 pl-44 w-[45%] shadow-lg clip-diagonal-top-left">
                    <div class="container relative w-full">
                        <h3 class="text-2xl text-red-600 font-bold font-anton mb-2">¡Hey! Aquí también puedes
                            contactarnos.
                        </h3>
                        <form class="space-y-4 font-outfit">
                            <input type="text" placeholder="Tu nombre"
                                class="w-full p-1 bg-transparent border-b-2 border-black placeholder-black focus:outline-none">
                            <input type="email" placeholder="Tu correo electrónico"
                                class="w-full p-1 bg-transparent border-b-2 border-black placeholder-black focus:outline-none">
                            <textarea rows="4" placeholder="Tu mensaje, saludo o sugerencia"
                                class="w-full p-1 bg-transparent border-b-2 border-black placeholder-black focus:outline-none"></textarea>
                            <button type="submit"
                                class="px-3 py-1 bg-black text-white font-bold hover:bg-red-600 hover:text-white transition">
                                ENVIAR
                            </button>
                        </form>
                    </div>
                </div>
            </div>
        </div>
        <div class="lg:hidden flex flex-col items-center gap-3">
            <div
                class="w-full bg-red-600 clip-diagonal-first-block z-10 flex items-center justify-center shadow-xl p-6">
                <h2 class="text-white text-5xl font-semibold font-anton">CONTÁCTANOS</h2>
            </div>

            <div class="bg-white/80 p-4 w-full max-w-sm shadow-lg clip-diagonal-top-right">
                <h3 class="text-2xl text-red-600 font-bold font-anton mb-2">ESCRÍBENOS</h3>
                <p class="font-outfit text-base mb-2">
                    ¿Tienes dudas? ¿Quieres sumarte? <br> ¡Mándanos tu mensaje!
                </p>
                <ul class="font-outfit text-sm space-y-1 mt-4">
                    <li><strong>Email: </strong> contacto@sumochile.cl</li>
                    <li><strong>Instagram: </strong>@sumochile</li>
                    <li><strong>Facebook: </strong>Federación Chilena de Sumo.</li>
                    <li><strong>Tiktok: </strong>@sumochile</li>
                </ul>
            </div>

            <div class="bg-white/80 p-2 w-full max-w-sm shadow-lg my-9">
                <div class="p-2">
                    <h3 class="text-xl text-red-600 font-bold font-anton mb-2">¡Hey! Aquí también puedes contactarnos.
                    </h3>
                    <form class="space-y-4 font-outfit">
                        <input type="text" placeholder="Tu nombre"
                            class="w-full p-1 bg-transparent border-b-2 border-black placeholder-black focus:outline-none">
                        <input type="email" placeholder="Tu correo electrónico"
                            class="w-full p-1 bg-transparent border-b-2 border-black placeholder-black focus:outline-none">
                        <textarea rows="4" placeholder="Tu mensaje, saludo o sugerencia"
                            class="w-full p-1 bg-transparent border-b-2 border-black placeholder-black focus:outline-none"></textarea>
                        <button type="submit"
                            class="px-3 py-1 bg-black text-white font-bold hover:bg-red-600 hover:text-white transition">
                            ENVIAR
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>
.clip-diagonal-first-block {
    clip-path: polygon(0 100%, 11.3% 0, 100% 0, 100% 100%);
}

.clip-diagonal-top-right {
    clip-path: polygon(0 0, 100% 0, 70% 100%, 0 100%);
}

.clip-diagonal-top-left {
    clip-path: polygon(0% 100%, 30% 0%, 100% 0%, 100% 100%);
}

.font-anton {
    font-family: "Anton", sans-serif;
}

.font-outfit {
    font-family: "Outfit", sans-serif;
}
</style>