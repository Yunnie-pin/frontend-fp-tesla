
<template>

        <!-- Section contact start -->
        <section id="contact">
            <div>
                <div class="py-12 px-6 md:px-20 bg-primary-white text-primary-black">
                    <div class="drop-shadow-xl bg-gray-100 rounded-lg pb-12">
                        <h2
                            class="text-primary-black drop-shadow-xl font-medium text-3xl pb-6 text-center pt-10">
                            Hubungi Kami</h2>   
                        <p class="text-light text-center px-8 lg:px-44 text-primary-black pb-12">For further questions,
                            including partnership opportunities, please email hello@creative-tim.com or contact using
                            our contact form.</p>

                        <form id="contact" v-on:submit="submitForm()">
                            <div class="lg:grid lg:grid-cols-2 justify-center gap-8 pb-4">
                                <div class="px-4 md:px-24 pb-4 lg:pr-0">
                                    <div class="text-light pb-2 text-primary-black font-bold">Full Name</div>
                                    <input type="text"
                                        class="border-2 border-gray-300 w-full maxmd: px-2 py-2 self-center rounded-lg"
                                        placeholder="Full Name" aria-label="Full Name" id="name" v-model="form.name">
                                </div>
                                <div class="px-4 md:px-24 pb-4 lg:pl-0">
                                    <div class="text-light pb-2 text-primary-black font-bold">Email</div>
                                    <input type="text"
                                        class="border-2 border-gray-300 w-full px-2 py-2 self-center rounded-lg"
                                        placeholder="hello@creative-tim.com" aria-label="Email" id="email" v-model="form.email">
                                </div>
                            </div>

                            <div class="px-4 md:px-24 pb-4">
                                <div class="text-light pb-2 text-primary-black font-bold">How can we help you?</div>
                                    <input class="inputBox border-2 border-gray-300 w-full px-2 pt-2 pb-12 self-center rounded-lg"
                                        placeholder="Describe your problem in at least 250 characters" id="message" v-model="form.message">


                                <button type="submit" class="mx-auto w-44 py-3 mt-4 font-sans font-bold bg-primary-black rounded-lg text-xs text-white text-center place-self-center">
                                    SEND MESSAGE</button>
                                <div>{{confirmation}}</div>

                            </div>
                        </form>



                    </div>

                </div>
            </div>
        </section>
        <!-- Section contact end -->
</template>

<script>
import axios from 'axios';

export default {
    name: "App",
    data(){
        return{
            confirmation: "",
            form: {
                name: '',
                email: '',
                message: ''
            }
        }
    },

    methods:{
        submitForm(){
            axios.post('http://127.0.0.1:8080/api/messages', this.form)
                 .then((res) => {
                    console.log(res);
                    this.form = res.data;
                        if (response.status == 200) {
                            this.confirmation = "Pesan Terkirim"
                        }
                    


                 })
                 .catch((error) => {
                    console.log(error);
                 }).finally(() => {
                 });
        }
    }
}
</script>

<style scoped>
</style>
