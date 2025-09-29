<script setup>
const posts = [
    {
        title: 'Campeonato Sudamericano de Sumo, Brasil 2025',
        excerpt: 'Una emocionante aventura para todos los sumotori chilenos',
        cover: '/img/brasil.png',
        date: '16 mayo 2025'
    },
    {
        title: 'Técnicas de entrenamiento en el Sumo',
        excerpt: 'Ahondamos en las técnicas de entrenamiento que hacen a los mejores sumotori',
        cover: '/img/fight.jpg',
        date: '16 mayo 2025'
    },
    {
        title: 'Nuestro Sensei Felipe Castro',
        excerpt: 'Conversamos con el Sensei Felipe Castro sobre su trayectoria y visión del Sumo en Chile',
        cover: '/img/felipecasb.png',
        date: '16 mayo 2025'
    }
]
</script>

<template>
    <section class="relative bg-cover bg-center bg-no-repeat px-4 md:px-6 py-24 min-h-screen"
        style="background-image: url('/img/blogbg.jpg');">

        <!-- Trapezoide encabezado -->
        <div
            class="trapezoid absolute top-0 left-1 w-[95vw] h-32 md:h-40 text-center bg-red-600 text-white px-4 py-4 md:px-10 md:py-6 flex flex-col justify-center z-10">
            <h1 class="titulo text-4xl md:text-6xl mt-2 leading-tight">Lo que pasa en el Dohyo</h1>
            <h2 class="subtitulo text-xl md:text-3xl text-black -mt-1">Blog_</h2>
        </div>

        <!-- Tarjetas de posts -->
        <div class="relative z-20 mt-20 md:mt-40 flex flex-wrap justify-center gap-10 md:gap-40 max-w-7xl mx-auto">
            <div v-for="(post, index) in posts" :key="index"
                class="w-full max-w-xs bg-white/60 backdrop-blur-md border p-4 shadow-2xl hover:scale-105 transition-all duration-300">
                <img :src="post.cover" alt="Portada del post" class="w-full h-44 object-cover mb-3" />
                <div class="flex flex-col h-full">
                    <h3 class="font-anton text-xl md:text-2xl mb-2 leading-tight">
                        {{ post.title }}
                    </h3>
                    <p class="font-outfit text-xs md:text-sm text-gray-700 mb-1">{{ post.date }}</p>
                    <p class="font-outfit text-sm text-gray-800 my-2 md:my-4">
                        {{ post.excerpt }}
                        <span class="ml-2 text-red-700 font-bold underline cursor-pointer">Leer más...</span>
                    </p>
                </div>
            </div>
        </div>

        <!-- Footer call-to-action -->
        <div
            class="absolute bottom-0 left-1/2 transform -translate-x-1/2 text-center w-full h-16 md:h-20 bg-red-600/90">
            <p class="font-anton text-white pt-3 md:pt-4 text-2xl md:text-4xl">IR AL BLOG</p>
        </div>
    </section>
</template>

<style scoped>
.titulo,
.subtitulo,
.font-anton {
    font-family: "Anton", sans-serif;
}

.font-outfit {
    font-family: "Outfit", sans-serif;
}

.trapezoid {
    clip-path: polygon(0 0%, 100% 0%, 90% 100%, 10% 100%);
}
</style>
