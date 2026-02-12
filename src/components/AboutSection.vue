<template>
    <section>
        <div class="text-white mt-18" id="about">
            <div class="absolute z-0 top-[93rem] inset-x-0 h-64 flex items-start">
                <div class="h-24 w-64 bg-gradient-to-br from-primary via-secondary blur-2xl to-[#570cac] opacity-20 "></div>
            </div>
        </div>
        <div class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-16 sm:py-16 xl:px-16 z-1">
            <div data-aos="flip-right">
                <h2 class="text-4xl font-bold text-white text-left mb-8">My Education</h2>
                <div class="space-y-8 py-8">
                    <div v-for="element in education" :key="element.id"
                    class="flex items-center md:w-[80%] w-full rounded-xl bg-[#111a3e] shadow-lg border-[#1f1641]"
                    >
                    <div class="h-16 w-16 flex items-center justify-center">
                        <img src="https://img.icons8.com/?size=100&id=hDuB3ilOaH8Z&format=png&color=ffffff" alt="graduation-cap--v1">
                    </div>
                    <div>
                        <h3 class="text-2xl font-semibold uppercase text-orange-400 lg:text-xl">
                            {{ element.School }}
                        </h3>
                        <p class="text-white">{{ element.program }}</p>
                        <p class="text-white">{{ element.year }}</p>
                    </div>
                </div>
                </div>
            </div>
            <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full" data-aos="flip-right">
                <h2 class="text-4xl font-bold md:text-center text-left mb-4">
                    <span class="text-white">More</span>

                    <span class="text-orange-400"> About</span>

                    <span class="text-white"> Me</span>
                </h2>
                <p class="text-white text-base lg:text-lg mt-8 py-8">Lorem ipsum dolor sit amet consectetur adipisicing elit.
                     Deleniti quas saepe quo, fugit molestias unde 
                     dignissimos consectetur a repellat excepturi.
                     Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                     Impedit amet laudantium maiores consequuntur, similique, 
                     soluta fugiat suscipit magni odit inventore minus dolorum corrupti quam,
                     quaerat ab nihil iste asperiores velit.
                    </p>
                    <div class="grid grid-cols-3 gap-3 max-w-lg pt-8">
                        <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3">
                            <h3 class="text-white font-bold text-xl sm:text-2xl lg:text-3xl">+200</h3>
                            <p class="text-sm sm:text-base text-gray-300">Happy Client</p>
                        </div>
                         <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3">
                            <h3 class="text-white font-bold text-xl sm:text-2xl lg:text-3xl">+300</h3>
                            <p class="text-sm sm:text-base text-gray-300">Project</p>
                        </div>
                    
                        <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3">
                            <h3 class="text-white font-bold text-xl sm:text-2xl lg:text-3xl">+7</h3>
                            <p class="text-sm sm:text-base text-gray-300">Year Experience</p>
                        </div>
                    </div>
            </div>
        </div>

    </section>
</template>
<script setup>
import { ref } from 'vue';
const education=ref([
    {
        id:1,
        School:'school 1',
        program: 'Software Engineer',
        year: '2022'
    },
    {
         id:2,
        School:'school 2',
        program: 'Cyber Security',
        year: '2024'
    },
    
])
</script>