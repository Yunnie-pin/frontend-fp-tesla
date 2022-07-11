
<template>

        <!-- Section team start -->
        <section id="team">
            <div>
                <div class="mx-auto">
                    <div class="bg-primary-black py-24">

                          <li v-for="team of teams" :key="team.id" class="text-white">
                            {{ team.name }}
                          </li>

                        <div class="team">
                            <h2 class="text-white font-sans font-medium text-3xl pb-16 text-center pt-10">Team</h2>
                          </div>
              
                          <div class="flex flex-wrap-reverse justify-center gap-16 lg:w-3/5 mx-auto pb-8">

                            <!--Isi konten Teams-->
                            

                            <div class="Arifin w-40">
                                <img src="../assets/image/team/pin.png" class="border-8 border-white rounded-full h-auto w-36" />
                                <div class="m-4 flex flex-col justify-center">
                                  <span class="font-bold font-sans text-white text-center"> Frontend Dev </span>
                                  <span class="block font-sans text-white text-sm text-center"> Arifin Yunianta </span>
                                  <span class="block font-sans text-white text-sm text-center">20.11.3763</span>
                                </div>
                              </div>
                
                              <div class="Zaky w-40">
                                <img src="../assets/image/team/zak.jpg" class="border-8 border-white rounded-full h-auto w-36" />
                                <div class="m-4 flex flex-col justify-center">
                                  <span class="font-bold font-sans text-white text-center"> Frontend Dev </span>
                                  <span class="block font-sans text-white text-sm text-center"> M Zaky Nurrokhman </span>
                                  <span class="block font-light font-sans text-white text-sm text-center">20.11.3791</span>
                                </div>
                              </div>
                
                              <div class="Icha w-40">
                                <img src="../assets/image/team/ic.jpg" class="border-8 border-white rounded-full h-auto w-36" />
                                <div class="m-4 flex flex-col justify-center">
                                  <span class="font-bold font-sans text-white text-center"> Frontend Dev </span>
                                  <span class="block font-sans text-white text-sm text-center"> Farichaturrifqi A </span>
                                  <span class="block font-light font-sans text-white text-sm text-center">20.11.3739</span>
                                </div>
                              </div>
                
                              <div class="Kendi w-40">
                                <img src="../assets/image/team/ken.jpg" class="border-8 border-white rounded-full h-auto w-36" />
                                <div class="m-4 flex flex-col justify-center">
                                  <span class="font-bold font-sans text-white text-center"> Backend Dev </span>
                                  <span class="block font-sans text-white text-sm text-center"> Ken Diani Mutia Sari </span>
                                  <span class="block font-sans text-white text-sm text-center">20.11.3736</span>
                                </div>
                              </div>

                            <div class="anas w-40">
                              <img src="../assets/image/team/an.jpg" alt="stew" class="border-8 border-white rounded-full h-auto w-36" />
                              <div class="m-4 flex flex-col justify-center">
                                <span class="font-bold font-sans text-white text-center"> Backend Dev </span>
                                <span class="block font-sans text-white text-center text-sm"> Anas Fikri Hanif </span>
                                <span class="block font-sans text-white text-center text-sm">20.11.3743</span>
                              </div>
                            </div>
              
                            <div class="ade w-40">
                              <img src="../assets/image/team/ad.jpeg" alt="stew" class="border-8 border-white rounded-full h-auto w-36" />
                              <div class="m-4 flex flex-col justify-center">
                                <span class="font-bold font-sans text-white text-center"> UI/UX Designer </span>
                                <span class="block font-sans text-white text-center text-sm"> Ade Febrian </span>
                                <span class="block font-sans text-white text-center text-sm">20.11.3793</span>
                              </div>
                            </div>
              
                            <div class="Faza w-40">
                              <img src="../assets/image/team/faz.jpg" alt="stew" class="border-8 border-white rounded-full h-auto w-36" />
                              <div class="m-4 flex flex-col justify-center">
                                <span class="font-bold font-sans text-white text-center"> Backend Dev </span>
                                <span class="block font-sans text-white text-sm text-center"> Faza Iman Imron </span>
                                <span class="block font-sans text-white text-sm text-center">20.11.3739</span>
                              </div>
                            </div>
              
                            <!--Akhir si konten Teams--> 
                          </div>
                    </div>
                </div>
                
                
            </div>
        </section>
        <!-- Section team end -->
</template>

<script>

import axios from "axios"
export default {
  name: "App",
  data() {
    return {
      teams: [],
    };
  },

  created() {
  axios({
      url: "http://localhost:8080/api/teams",
      method: "get",
      headers: { "Access-Control-Allow-Origin": "*" },
    })
      .then(function (response) {
        this.teams = response.data
        console.log(response.data);
      })
      .catch(function (error) {
        console.log(error);
      });
  },
};


</script>

<style scoped>
</style>
