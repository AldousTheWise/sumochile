<script setup>
import brasilImg from '@/assets/img/brasil.png';
import fightImg from '@/assets/img/fight.jpg';
import felipeCastImg from '@/assets/img/felipecasb.png';
import blogBgImg from '@/assets/img/blogbg.jpg';

const posts = [
    {
        title: 'Campeonato Sudamericano de Sumo, Brasil 2025',
        excerpt: 'Una emocionante aventura para todos los sumotori chilenos',
        cover: brasilImg,
        date: '16 mayo 2025'
    },
    {
        title: 'Técnicas de entrenamiento en el Sumo',
        excerpt: 'Ahondamos en las técnicas de entrenamiento que hacen a los mejores sumotori',
        cover: fightImg,
        date: '16 mayo 2025'
    },
    {
        title: 'Nuestro Sensei Felipe Castro',
        excerpt: 'Conversamos con el Sensei Felipe Castro sobre su trayectoria y visión del Sumo en Chile',
        cover: felipeCastImg,
        date: '16 mayo 2025'
    }
]
</script>

<template>
    <section class="relative bg-cover bg-center bg-no-repeat px-0 lg:px-6 lg:py-24 h-[70dvh] lg:min-h-[115dvh]"
        :style="{ backgroundImage: `url(${blogBgImg})` }">
        <div class="hidden lg:block">
            <div
                class="trapezoid absolute top-0 left-10 w-[93dvw] h-40 text-center bg-red-600 text-white px-10 py-6 flex flex-col justify-center z-10">
                <h2 class="text-6xl font-anton mt-2 leading-tight">Lo que pasa en el Dohyo</h2>
                <h3 class="text-3xl font-anton text-black -mt-1">Blog_</h3>
            </div>

            <div class="relative z-20 flex flex-wrap justify-center gap-12 max-w-7xl mb-40 mt-25">
                <div v-for="(post, index) in posts" :key="index"
                    class="w-full max-w-xs bg-white/60 backdrop-blur-md border p-4 shadow-2xl hover:scale-105 transition-all duration-300">
                    <img :src="post.cover" alt="Portada del post" class="w-full h-44 object-cover mb-3" />
                    <div class="flex flex-col h-full">
                        <h3 class="font-anton text-2xl mb-2 leading-tight">
                            {{ post.title }}
                        </h3>
                        <p class="font-outfit text-sm text-gray-700 mb-1">{{ post.date }}</p>
                        <p class="font-outfit text-sm text-gray-800 my-4">
                            {{ post.excerpt }}
                            <a href="#" class="ml-2 text-red-700 font-bold underline">Leer más...</a>
                        </p>
                    </div>
                </div>
            </div>

            <div
                class="absolute bottom-0 left-1/2 transform -translate-x-1/2 text-center w-full h-20 py-3 bg-red-600/90">
                <h2 class="font-anton text-white text-6xl">IR AL BLOG</h2>
            </div>
        </div>

        <div class="lg:hidden flex flex-col h-full">
            <div class="w-full h-32 text-center bg-red-600 text-white px-4 py-4 flex flex-col justify-center z-10">
                <h2 class="text-4xl leading-tight font-anton">Lo que pasa en el Dohyo</h2>
                <h3 class="text-xl text-black -mt-1 font-anton">Blog_</h3>
            </div>

            <div class="flex-grow pt-3">
                <div class="flex overflow-x-auto py-8 px-4 gap-6 w-full snap-x snap-mandatory">
                    <div v-for="(post, index) in posts" :key="index"
                        class="flex-shrink-0 w-[80%] max-w-xs bg-white/60 backdrop-blur-md border p-4 shadow-xl snap-center">
                        <img :src="post.cover" alt="Portada del post" class="w-full h-44 object-cover mb-3" />
                        <div>
                            <h3 class="font-anton text-xl mb-2 leading-tight">
                                {{ post.title }}
                            </h3>
                            <p class="font-outfit text-xs text-gray-700 mb-1">{{ post.date }}</p>
                            <p class="font-outfit text-sm text-gray-800 my-2">
                                {{ post.excerpt }}
                                <a href="#" class="ml-2 text-red-700 font-bold underline">Leer más...</a>
                            </p>
                        </div>
                    </div>
                </div>
            </div>
            <div
                class="absolute bottom-0 left-1/2 transform -translate-x-1/2 text-center w-full h-15 py-3 bg-red-600/90">
                <h2 class="font-anton text-white text-4xl">IR AL BLOG</h2>
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

.trapezoid {
    clip-path: polygon(0 0%, 100% 0%, 90% 100%, 10% 100%);
}

.overflow-x-auto {
    scrollbar-width: none;
}

.overflow-x-auto::-webkit-scrollbar {
    display: none;
}
</style>
