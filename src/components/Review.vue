
<template>
        <section id="Review">
            <div class=" bg-primary-black pb-4">
                <div class="max-w-screen-xl mx-auto">
                    <h2 class="text-white text-center text-3xl py-10 font-medium">Review</h2>

                    <div v-for="review of reviews" :key="review.id">
                        <div v-if="review.id % 2 == 1">
                        
                                                <div class="flex flex-wrap lg:grid lg:grid-cols-2 pb-10">

                            <div class="px-10 lg:order-2 pb-10">

                                <div class="flex wrap gap-4 pb-6">
                                    <div class="flex-1 mx-auto">
                                        <h2 class="text-white font-medium">{{review.name}}</h2>
                                        <h2 class="text-white pb-2 font-light">{{review.position}}</h2>
                                        <hr class="pb-2">
                                        <img src="dist/image/review-star/5.png" alt="star" class="drop-shadow-xl">
                                    </div>

                                    <img src="dist/image/produk/avatar/avatar1.png" alt="gambarprofile1"
                                        class="block h-24 rounded-full flex-none border-6">
                                </div>

                                <div>
                                    <p class="font-sans text-base text-white text-justify italic">{{review.comment}} </p>
                                </div>
                            </div>

                            <div class="lg:order-1">
                                <img src="dist/image/produk/img/reviewproduct1.png" alt="mobil1"
                                    class="lg:float-right mx-auto rounded-3xl drop-shadow-xl maxmd:hidden">
                            </div>
                        </div>


                        </div>

                        <div v-else>
                            <div class="flex flex-wrap lg:grid lg:grid-cols-2 pb-10">

                                <div class="px-10 pb-10">

                                    <div class="flex wrap gap-4 pb-6 float">
                                        <div class="flex-1 mx-auto">
                                            <h2 class="text-white font-medium">{{review.name}}</h2>
                                            <h2 class="text-white pb-2 font-light">{{review.position}}</h2>
                                            <hr class="pb-2">
                                            <img src="dist/image/review-star/5.png" alt="star" class="drop-shadow-xl">
                                        </div>

                                        <img src="dist/image/produk/avatar/avatar2.png" alt="gambarprofile1"
                                            class="block h-24 rounded-full flex-none border-6 ">
                                    </div>

                                    <div>
                                        <p class="font-sans text-base text-white text-justify italic">{{review.comment}}</p>
                                    </div>
                                </div>

                                <div>
                                    <img src="dist/image/produk/img/reviewproduct2.png" alt="mobil2"
                                        class="lg:float-left rounded-3xl drop-shadow-xl maxmd:hidden">
                                </div>
                            </div>
                        </div>

                    </div>
                </div>

            </div>
        </section>
        <!-- Section review end -->
</template>

<script>
import axios from "axios"
export default {
  name: "App",
  data() {
    return {
      reviews: [],
    };
  },
created() {
    axios
      .get(`http://localhost:8080/api/reviews`)
      .then((response) => {
        console.log(response.data);
        this.reviews = response.data;
      })
      .catch((e) => {
        console.log(e);
      });
  },
};

</script>


<style scoped>
</style>
