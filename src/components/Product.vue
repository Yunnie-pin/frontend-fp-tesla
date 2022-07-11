<script setup>

import { ref } from 'vue'

const isOn = ref(true)

function togglePopUp() {
  isOn.value = !isOn.value
}

</script>

<template>

    <div id="blur-container"  :class="{'hidden': isOn}"
    class="fixed z-[999] top-0 w-screen h-screen backdrop-blur-sm" >
    </div>

        <!-- Berisi konten yang akan ditampilkan -->
        <section id="home" class="filter-none">
            <!-- Slider main container -->
            <div class="swiper">
                <!-- Additional required wrapper -->
                <div class="swiper-wrapper">
                    <!-- Slides -->
                    <div class="swiper-slide"><img src="dist/image/cars/slider/crop-M3-Homepage-Desktop-LHD.jpg"
                            alt="Model 3" class="w-full"></div>
                    <div class="swiper-slide"><img src="dist/image/cars/slider/crop-Desktop-ModelY.jpg" alt="Model Y"
                            class="w-full"></div>
                    <div class="swiper-slide"><img src="dist/image/cars/slider/crop-Homepage-Model-S-Desktop-LHD.jpg"
                            alt="Model S" class="w-full"></div>
                    <div class="swiper-slide"><img src="dist/image/cars/slider/crop-Homepage-Model-X-Desktop-LHD.jpg"
                            alt="Model X" class="w-full"></div>
                </div>
                <!-- If we need pagination -->
                <div class="swiper-pagination"></div>

                <!-- If we need navigation buttons -->
                <!-- <div class="swiper-button-prev text-transparent"></div> -->
                <!-- <div class="swiper-button-next text-slate-500"></div> -->
            </div>
        </section>

        <!-- Section produk start -->
        <section id="product">
            <div class="bg-slate-50">
                <h2 class="text-center text-3xl py-10 bg-slate-50 font-medium">Produk</h2>
                <div class="flex flex-wrap justify-center">
                    <!-- Button -->
                    <div class="flex flex-wrap flex-row md:flex-col">
                        <button id="button-model-3"
                            class="font-bold focus:bg-slate-900 focus:text-white w-fit mx-auto my-3 px-5 py-2 rounded-xl">Model
                            3</button>
                        <button id="button-model-y"
                            class="font-bold focus:bg-slate-900 focus:text-white w-fit mx-auto my-3 px-5 py-2 rounded-xl">Model
                            Y</button>
                        <button id="button-model-s"
                            class="font-bold focus:bg-slate-900 focus:text-white w-fit mx-auto my-3 px-5 py-2 rounded-xl">Model
                            S</button>
                        <button id="button-model-x"
                            class="font-bold focus:bg-slate-900 focus:text-white w-fit mx-auto my-3 px-5 py-2 rounded-xl">Model
                            X</button>
                    </div>

                    <!-- Product image -->
                    <img id="model-3" src="dist/image/cars/produk/Model 3.png" alt="model 3"
                        class="w-[500px] h-fit px-5">
                    <img id="model-y" src="dist/image/cars/produk/Model Y.png" alt="model Y"
                        class="hidden w-[500px] h-fit px-5">
                    <img id="model-s" src="dist/image/cars/produk/Model S.png" alt="model S"
                        class="hidden w-[500px] h-fit px-5">
                    <img id="model-x" src="dist/image/cars/produk/Model X.png" alt="model X"
                        class="hidden w-[500px] h-fit px-5">

                    <!-- Product menu button -->
                    <div class="flex flex-col">
                        <!-- Menu produk -->
                        <div class="flex flex-wrap justify-center">
                            <button id="spesifikasi"
                                class="font-bold focus:bg-slate-900 focus:text-white w-fit h-fit mx-9 my-3 px-5 py-2 rounded-xl">
                                Spesifikasi
                            </button>
                            <button id="detail-fitur" @click="togglePopUp"
                                class="font-bold focus:bg-slate-900 focus:text-white w-fit h-fit mx-9 my-3 px-5 py-2 rounded-xl">
                                Detail Fitur
                            </button>
                            <button id="beli-sekarang"
                                class="font-bold focus:bg-slate-900 focus:text-white w-fit h-fit mx-9 my-3 px-5 py-2 rounded-xl">
                                Beli Sekarang
                            </button>
                        </div>

                        <!-- Keterangan spesifikasi -->
                        <div class="grid grid-cols-3 text-center">
                            <div class="lg:mx-5 lg:my-2">
                                <p class="font-bold text-lg">200 mph</p>
                                <p class="text-xs">Top Speed</p>
                            </div>
                            <div class="lg:mx-5 lg:my-2">
                                <p class="font-bold text-lg">396 mi</p>
                                <p class="text-xs">Range</p>
                            </div>
                            <div class="lg:mx-5 lg:my-2">
                                <p class="font-bold text-lg">$95,840</p>
                                <p class="text-xs">Model S</p>
                            </div>
                            <div class="lg:mx-5 lg:my-2">
                                <p class="font-bold text-lg">1,020 hp</p>
                                <p class="text-xs">Peak Power</p>
                            </div>
                            <div class="lg:mx-5 lg:my-2">
                                <p class="font-bold text-lg">1.99 s</p>
                                <p class="text-xs">0-60 mph</p>
                            </div>
                            <div class="lg:mx-5 lg:my-2">
                                <p class="font-bold text-lg">$126,840</p>
                                <p class="text-xs">Model S Paid</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Pop up detail fitur -->
                <!-- Slider main container -->
                <div id="pop-up" :class="{'hidden': isOn}"
                    class="swiper fixed z-[9999] top-0 bottom-0 left-0 right-0 m-auto bg-white w-2/3 h-[500px] rounded-3xl transition duration-300">
                    <!-- Additional required wrapper -->
                    <div class="swiper-wrapper">
                        <!-- Slides -->
                        <!-- Slide 1 -->
                        <div
                            class="swiper-slide justify-center items-center flex flex-wrap overflow-auto lg:overflow-hidden">
                            <img src="dist/image/cars/detail produk/S3XY_StdFeat_Autopilot.jpg" alt="Auto Pilot"
                                class="w-2/3 lg:h-min lg:w-1/2 lg:flex-1">
                            <div class="m-10 w-fit lg:flex-1">
                                <h3 class="my-3 font-bold text-lg">Auto Pilot</h3>
                                <p class="text-sm">
                                    Termasuk dalam setiap Tesla, Autopilot memungkinkan mobil Anda untuk menyetir,
                                    mempercepat, dan mengerem secara otomatis untuk kendaraan lain dan pejalan kaki di
                                    dalam
                                    jalurnya. Fitur keselamatan dan kenyamanan canggih dirancang untuk membantu Anda
                                    dengan
                                    bagian yang paling memberatkan dalam berkendara, di samping fitur bantuan pengemudi
                                    seperti pengereman darurat, peringatan tabrakan, dan pemantauan blind-spot.
                                </p>
                            </div>
                        </div>

                        <!-- Slide 2 -->
                        <div class="swiper-slide justify-center items-center flex flex-wrap overflow-auto">
                            <img src="dist/image/cars/detail produk/Chargeport_SX.jpg" alt="Easy Charging"
                                class="w-2/3 lg:h-min lg:w-1/2 lg:flex-1">
                            <div class="m-10 w-fit lg:flex-1">
                                <h3 class="my-3 font-bold text-lg">Easy Charging</h3>
                                <p class="text-sm">
                                    Charge anywhere there is electricity. Most range used for daily driving can be
                                    topped
                                    off using the Mobile Connector Bundle and a 110V household outlet, or upgrade to a
                                    220V
                                    Tesla Wall Connector for the best home charging experience. For long distance
                                    travel,
                                    Model 3 adds up to 175 miles of range in just 15 minutes using Tesla's Supercharger
                                    network, getting you back on the road, sooner.
                                </p>
                            </div>
                        </div>

                        <!-- Slide 3 -->
                        <div class="swiper-slide justify-center items-center flex flex-wrap overflow-auto">
                            <img src="dist/image/cars/detail produk/Model_S_mobile_app.jpeg" alt="Mobile App"
                                class="w-2/3 lg:h-min lg:w-1/2 lg:flex-1">
                            <div class="m-10 w-fit lg:flex-1">
                                <h3 class="my-3 font-bold text-lg">Tesla Mobile App</h3>
                                <p class="text-sm">
                                    Remotely control and monitor your Tesla with Phone Key keyless driving, range &
                                    charging
                                    status, climate control, live GPS location and more. You can even schedule service
                                    and
                                    monitor your entire Tesla ecosystem, including power flow from Powerwall or from
                                    Solar
                                    Roof and Solar Panels.
                                </p>
                            </div>
                        </div>
                    </div>
                    <!-- If we need pagination -->
                    <div class="swiper-pagination"></div>

                    <!-- If we need navigation buttons -->
                    <!-- <div class="swiper-button-prev"></div> -->
                    <!-- <div class="swiper-button-next"></div> -->

                    <!-- If we need scrollbar -->
                    <!-- <div class="swiper-scrollbar"></div> -->
                </div>
                
                <div class="flex flex-wrap lg:flex-nowrap px-5 py-28 lg:px-28 md:px-14 xs:p-1">
                    <div class="m-5">
                        <h3 class="my-2 font-bold">Stay Connected</h3>
                        <p>
                            Instantly connect with multi device Bluetooth, or fast charge devices with wireless and 36-watt USB-C charging.
                        </p>
                    </div>
                    <div class="m-5">
                        <h3 class="my-2 font-bold">Immersive Sound</h3>
                        <p>
                            A 22-speaker, 960-watt audio system with Active Road Noise Reduction offers immersive listening and studio-grade sound quality.
                        </p>
                    </div>
                    <div class="m-5">
                        <h3 class="my-2 font-bold">Room for Everything</h3>
                        <p>
                            With front and rear trunks and fold-flat seats you can fit your bike without taking the wheel off—and your luggage too.
                        </p>
                    </div>
                </div>

                <!-- <img src="dist/image/cars/MS-Exterior-Hero-Destop.jpg" alt="Air Flow" class="w-full"> -->
                <div class="bg-fixed h-[100vmin] lg:h-screen"
                    style="background-image: url(dist/image/cars/MS-Exterior-Hero-Desktop.jpg); background-position: center; background-repeat: no-repeat; background-size: 100vmax;">
                </div>

                <div class="flex flex-wrap lg:flex-nowrap px-5 py-28 lg:px-28 md:px-14 xs:p-1">
                    <div class="m-5">
                        <h3 class="my-2 font-bold">Relentless Performance</h3>
                        <p>
                            Staggered, performance wheels and tires keep the car planted and help transfer maximum power down to the road.
                        </p>
                    </div>
                    <div class="m-5">
                        <h3 class="my-2 font-bold">Optimized Aerodynamics</h3>
                        <p>
                            Attention to detail on all exterior surfaces makes Model S the most aerodynamic production car on Earth.
                        </p>
                    </div>
                    <div class="m-5">
                        <h3 class="my-2 font-bold">Refined Styling</h3>
                        <p>
                            An iconic silhouette meets refreshed, elegant proportions.
                        </p>
                    </div>
                </div>
            </div>
        </section>
        <!-- Section produk end -->


</template>

<style scoped>
</style>
