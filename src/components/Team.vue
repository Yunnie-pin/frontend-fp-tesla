
<template>

        <!-- Section team start -->
        <section id="team">
            <div>
                <div class="mx-auto">
                    <div class="bg-primary-black py-24">

                        <div class="team">
                            <h2 class="text-white font-sans font-medium text-3xl pb-16 text-center pt-10">Team</h2>
                          </div>
              
                          <div class="flex flex-wrap-reverse justify-center gap-16 lg:w-3/5 mx-auto pb-8">

                            <!--Isi konten Teams-->
                            
                            <div v-for="team of teams" :key="team.id">
                              <div class="Arifin w-40">
                                  <img :src="team.avatar" class="border-8 border-white rounded-full h-auto w-36" />
                                  <div class="m-4 flex flex-col justify-center">
                                    <span class="font-bold font-sans text-white text-center"> {{team.role}} </span>
                                    <span class="block font-sans text-white text-sm text-center"> {{ team.name }} </span>
                                    <span class="block font-sans text-white text-sm text-center">{{ team.id_card }}</span>
                                  </div>
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
    axios
      .get(`http://localhost:8080/api/teams`)
      .then((response) => {
        console.log(response.data);
        this.teams = response.data;
      })
      .catch((e) => {
        console.log(e);
      });
  },
};

</script>

<style scoped>
</style>
