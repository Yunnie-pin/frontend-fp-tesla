<script setup>

import { ref } from 'vue'

const isOn = ref(true)

function toggleHamburger() {
  isOn.value = !isOn.value
}


</script>

<template>
    <!-- Jalankan Tailwind dengan script: npm run start -->
    <!-- Jalankan Live Server dengan shortcut (Tahan)Alt + (Tekan)L (Kemudian)=> (Tekan)O (Bukan nol) -->
    <div id="blur-container" class="hidden fixed z-[999] top-0 w-screen h-screen backdrop-blur-sm">
    </div>

    <header class="transition duration-500 absolute top-0 left-0 w-full flex items-center z-[9999] justify-center">
        <div class="container">
            <div class="flex items-center justify-center relative py-2">
                <!-- Logo ketika hamburger muncul -->
                <div class="px-3 w-16 lg:hidden">
                    <a href="#home">
                        <img src="dist/image/logo.png" alt="logo">
                    </a>
                </div>

                <!-- Hamburger -->
                <div class="flex items-center w-full">
                    <button @click="toggleHamburger" :class="{'hamburger-active': isOn}" id="hamburger" name="hamburger" type="button" class="block absolute right-5 lg:hidden">
                        <span
                            class="w-[30px] h-0.5 my-2 block bg-black transition duration-300 ease-in-out origin-top-left"></span>
                        <span class="w-[30px] h-0.5 my-2 block bg-black transition duration-300 ease-in-out"></span>
                        <span
                            class="w-[30px] h-0.5 my-2 block bg-black transition duration-300 ease-in-out origin-bottom-left"></span>
                    </button>
                    <nav @click="toggleHamburger" :class="{'hidden': isOn}"
                        class="hidden bg-white/70 absolute right-4 max-w-[250px] w-full rounded-lg shadow-lg top-full justify-evenly lg:bg-transparent lg:shadow-none lg:flex lg:static lg:max-w-full lg:rounded-none">
                        <ul class="block lg:flex items-center w-full justify-evenly">
                            <li class="group">
                                <a href="#home"
                                    class="px-5 py-2 flex rounded-full transition duration-200 font-bold group-hover:bg-slate-200/75">
                                    Beranda
                                </a>
                            </li>
                            <li class="group">
                                <a href="#product"
                                    class="px-5 py-2 flex rounded-full transition duration-200 font-bold group-hover:bg-slate-200/75">
                                    Produk
                                </a>
                            </li>
                            <li class="group">
                                <a href="#about"
                                    class="px-5 py-2 flex rounded-full transition duration-200 font-bold group-hover:bg-slate-200/75">
                                    Tentang Kami
                                </a>
                            </li>
                        </ul>
                        <a href="#home" class="hidden lg:block">
                            <img src="dist/image/logo.png" alt="logo" class="w-20">
                        </a>
                        <ul class="block lg:flex items-center w-full justify-evenly">
                            <li class="group">
                                <a href="#team"
                                    class="px-5 py-2 flex rounded-full transition duration-200 font-bold group-hover:bg-slate-200/75">
                                    Team
                                </a>
                            </li>
                            <li class="group">
                                <a href="#contact"
                                    class="px-5 py-2 flex rounded-full transition duration-200 font-bold group-hover:bg-slate-200/75">
                                    Kontak Kami
                                </a>
                            </li>
                            <li class="group">
                                <a href="login.html"
                                    class="px-5 py-2 flex rounded-full transition duration-200 font-bold group-hover:bg-slate-200/75">
                                    Login
                                </a>
                            </li>
                        </ul>
                    </nav>
                </div>

            </div>
        </div>
        <!-- Berisi logo dan navigasi menu -->

    </header>


</template>

<style scoped>
</style>
