<template>
    <section class="relative bg-cover bg-center bg-no-repeat px-6 py-24 min-h-screen"
        style="background-image: url('/img/wrestler.png');">

        <div
            class="absolute w-[90%] h-[140px] top-0 right-0 bg-red-600 clip-diagonal-left z-10 flex items-center justify-center shadow-xl">
            <h1 class="text-white text-7xl font-semibold font-anton">CONTÁCTANOS</h1>
        </div>


        <div class="relative z-20 mt-[180px] max-w-6xl mx-auto flex justify-between gap-6" style="height: 320px;">

            <div class="bg-white/80 p-6 w-[45%] shadow-lg flex flex-col justify-between clip-diagonal-top-right"
                style="margin-top: 0;">
                <div>
                    <h2 class="text-2xl text-red-600 font-bold font-anton mb-2">ESCRÍBENOS</h2>
                    <p class="font-outfit text-lg mb-2">
                        ¿Tienes dudas? ¿Quieres sumarte? <br>Mándanos tu mensaje!
                    </p>
                </div>
                <ul class="font-outfit text-base space-y-1">
                    <li><strong>Email:</strong> contacto@sumochile.cl</li>
                    <li><strong>Teléfono:</strong> +56 9 1234 5678</li>
                    <li><strong>Instagram:</strong> @sumochile</li>
                </ul>
            </div>

            <div class="absolute right-0 top-5 bg-white/80 p-6 w-[45%]  shadow-lg flex flex-col justify-between clip-diagonal-top-left"
                style="margin-top: 80px;">
                <div class="container relative top-2  left-35 w-80">
                    <div>
                        <h2 class="text-2xl text-red-600 font-bold font-anton mb-2">FORMULARIO</h2>
                    </div>
                    <form class="space-y-2 font-outfit">
                        <input type="text" placeholder="Tu nombre"
                            class="w-full p-1 bg-transparent border-b-2 border-black placeholder-black focus:outline-none" />
                        <input type="email" placeholder="Tu correo"
                            class="w-full p-1 bg-transparent border-b-2 border-black placeholder-black focus:outline-none" />
                        <textarea rows="2" placeholder="Tu mensaje"
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
.clip-diagonal-left {
    clip-path: polygon(0 0, 100% 0, 100% 100%, 60px 100%);
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
