<template>
    <section class="text-white mt-18" id="skills">
        <div class="absolute right-0 top-[110rem] h-full justify-end">
            <span class="flex opacity-20">
            <span class="w-16 h-32 rounded-1-full flex bg-primary blur-2xl"></span>
            <span class="w-16 h-32 rounded-r-full flex bg-[#f88fc2] blur-2xl mt-14"></span>
            </span>
        </div>
        <div class="md:grid md:grid-cols-2 gap-8 items-center py-8 px-4 xl:gap-16 xl:px-16">
            <div class="mt-4 md:mt-0 text-left flex flex-col z-10 h-full w-[80%]">
                <h2 class="text-4xl font-bold text-white text-left mb-4">My
                    <span class="text-transparent bg-clip-text bg-gradient-to-r from-orange-400 to-yellow-400">Skills</span>
                </h2>
                <div class="mt-8 space-y-6" v-for="skill in Skills" :key="skill.id"
                :class="'w-full'"  data-aos="fade-right">
                <div class="flex justify-between mb-2">
                    <span class="font-medium text-white">{{ skill.name }}</span>
                    <span class="text-sm text-gray-300">{{ skill.width }}</span>
                </div>

                <div class="w-full h-1 bg-[#1f1641] rounded-full overflow-hidden">
                    <div
                    class="h-1 rounded-full bg-gradient-to-r from-orange-400 to-yellow-400 transition-all duration-700"
                    :style="{ width: skill.width}"
                    ></div>
                </div>
                </div>
            </div>
            <div data-aos="flip-left">
                <h2 class="text-4xl font-bold text-white text-left mb-8 md:text-center md:mt-0 mt-8">My Experiences</h2>
                <div class="space-y-8 py-8" data-aos="fade-left">
                    <div v-for="element in Experiences" key="element.id"
                    class="flex items-center rounded-xl p-4 bg-[#111a3e] shadow-lg border border-[#1f1641]"
                    >
                    <div  class="w-1/4">
                        <img src="https://img.icons8.com/?size=100&id=ScAViD0I8h4B&format=png&color=ffffff" alt="lawyer">
                    </div>
                    <div class="w-3/4 pl-4">
                        <h3 class="text-2xl font-semibold uppercase text-orange-400 lg:text-xl">
                            {{ element.role }}
                        </h3>
                        <p class="text-white">{{ element.company }}</p>
                        <p class="text-white">{{ element.date }}</p>
                    </div>
                </div>
                </div>
            </div>
        </div>
    </section>
</template>
<script setup>
import { ref } from 'vue';
const Skills =ref([
    {
        id:1,
        name: 'HTML & CSS',
        width: '85%'

    },
     {
        id:2,
        name: 'React',
        width: '85%'

    },
     {
        id:3,
        name: 'Python',
        width: '70%'

    },
     {
        id:4,
        name: 'JavaScript',
        width: '98%'

    },

]);
const Experiences =ref([
    {
        id:1,
        role:'Software Engineer',
        company:'Microsoft',
        date: 'May 2022 - June 2024'
    },
    {
        id:2,
        role:'Frontend Developer',
        company:'Spotify',
        date: 'July 2024 - January 2026'
    },
])
</script>