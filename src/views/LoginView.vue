<script setup>
import { ref } from 'vue';
import { useRouter } from 'vue-router';
import { useUserStore } from '@/stores/userStore';

const email = ref('');
const password = ref('');
const router = useRouter();
const userStore = useUserStore();

const login = () => {
    if (email.value && password.value) {
        userStore.setUser({ email: email.value });
        router.push('/');
    }
}
</script>

<template>
    <div class="min-h-screen flex justify-center items-center bg-gray-100">
        <form class="bg-white p-6 rounded-lg shadow-md w-96">
            <h2 class="text-2xl font-bold text-center mb-4">Iniciar sesión</h2>
            <input type="email" placeholder="Correo electrónico" v-model="email"
                class="w-full p-2 mmb-4 border border-gray-300 rounded" />
            <input type="password" placeholder="Contraseña" v-model="password"
                class="w-full p-2 mb-4 border border-gray-300 rounded" />
            <button @click="login" class="w-full bg-blue-600 text-white py-2 rounded hover:bg-blue-700">Iniciar
                Sesión</button>
        </form>
    </div>
</template>


<style scoped></style>