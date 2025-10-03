<script setup>
import aboutImage from '@/assets/img/about2.png';
import felipeImagen from '@/assets/img/felipe.webp';

const secciones = [
    {
        titulo: 'Nosotros',
        texto: 'Somos una organización deportiva nacional que se encarga de la enseñanza y la difusión del milenario arte marcial del Sumo en el país, dirigida por Felipe Castro, seleccionado nacional en la disciplina. Formamos parte de la International Sumo Federation.'
    },
    {
        isCard: true,
        nombre: 'Sensei Felipe Castro',
        descripcion: 'Seleccionado nacional en sumo tradicional.',
        img: felipeImagen
    },
    {
        titulo: 'Filosofía y Valores',
        texto: 'El sumo cultiva el respeto, la disciplina y la perseverancia. Más que fuerza, exige honor. Cada combate comienza y termina con un saludo, recordándonos que el rival no es un enemigo, sino un espejo de nuestro esfuerzo. En el dojo y en la vida, el camino del sumotori es humildad y entrega.'
    }
];
</script>

<template>
    <section class="relative h-[100dvh] overflow-hidden bg-black">

        <img :src="aboutImage" class="absolute inset-0 w-full h-full object-cover z-0" alt="Fondo" />

        <div
            class="absolute top-0 left-0 z-10 bg-white/80 py-5 px-10 clip-diagonal-right w-[60%] md:w-[60%] h-1/4 md:h-1/4">
            <h2 class="titulo text-red-600 text-4xl md:text-7xl font-bold mt-3 md:mt-7">Quiénes Somos</h2>
        </div>


        <div class="hidden md:flex absolute bottom-0 z-10 w-full justify-between items-end px-10 gap-8">
            <div class="w-1/4 bg-red-600/90 text-white p-6 self-end min-h-[400px]">
                <h3 class="titulo text-3xl mb-2">{{ secciones[0].titulo }}</h3>
                <p class="texto text-sm whitespace-pre-line">{{ secciones[0].texto }}</p>
            </div>

            <div class="bg-white/90 w-1/4 flex items-center gap-4 p-4 mb-10 rounded shadow-lg self-end">
                <img :src="secciones[1].img" class="w-20 h-20 object-cover rounded-full" :alt="secciones[1].nombre" />
                <div>
                    <h3 class="titulo text-red-600 text-xl">{{ secciones[1].nombre }}</h3>
                    <p class="texto text-sm text-black mt-1">{{ secciones[1].descripcion }}</p>
                </div>
            </div>

            <div class="w-1/4 bg-red-600/90 text-white p-6 self-end min-h-[400px]">
                <h3 class="titulo text-3xl mb-2">{{ secciones[2].titulo }}</h3>
                <p class="texto text-sm whitespace-pre-line">{{ secciones[2].texto }}</p>
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

.clip-diagonal-right {
    clip-path: polygon(0 0, 100% 0, 97% 100%, 0 100%);
}
</style>