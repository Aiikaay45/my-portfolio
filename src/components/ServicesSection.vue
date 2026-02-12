<template>
    <section class="text-white mt-20" id="services">
        <div class="px-4 xl:pl-16">
            <h2 class="text-4xl font-bold text-white mb-4">My Services</h2>
        </div>
        <div class="py-8 xl:px-16 px-4 sm:py-16 grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 lg:grid-cols-3 md:gap-10 md:pt-12  ">
            <div v-for="service in services" :key="service.id" data-aos="fade-up" class="px-8 py-12 rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641]">
                <div class="flex flex-col items-center text-center">
                    <div>
                        <img :src="service.icon" alt="service icon">
                    </div>
                    <div class="text-center">
                        <h3 class="pt-8 text-lg font-semibold uppercase text-orange-400 lg:text-xl">
                            {{ service.name }}
                        </h3>
                        <p class="text-grey pt-4 text-sm group-hover:text-white md:text-base">
                            {{ service.description }}
                        </p>
                    </div>
                </div>
            </div>
        </div>

    </section> 
</template>

<script setup>
import { ref } from 'vue';
const services =ref([
    {
        id:1,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/google-code.png',
        name:'WEB DEVELOPMENT',
        description:'Lorem ipsum dolor, sit amet consectetur adipisicing elit. In, quos!'
    },
    {
        id:2,
        icon:'https://img.icons8.com/?size=100&id=TAH7mJxpBhnm&format=png&color=ffffff',
        name:'Technical Writing',
        description:'Lorem ipsum dolor, sit amet consectetur adipisicing elit. In, quos!' 
    },
    {
         id:3,
        icon:'https://img.icons8.com/?size=100&id=qTi7dvhQWqxW&format=png&color=ffffff',
        name:'Mobile Development',
        description:'Lorem ipsum dolor, sit amet consectetur adipisicing elit. In, quos!'
    },
    {
         id:4,
        icon:'https://img.icons8.com/?size=100&id=wYZphVpCWsq5&format=png&color=ffffff',
        name:'Cyber Security',
        description:'Lorem ipsum dolor, sit amet consectetur adipisicing elit. In, quos!'
    },
    {
         id:5,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/windows10-personalization.png',
        name:'Graphic Design',
        description:'Lorem ipsum dolor, sit amet consectetur adipisicing elit. In, quos!'
    },
    {
         id:6,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/web-design.png',
        name:'Web Design',
        description:'Lorem ipsum dolor, sit amet consectetur adipisicing elit. In, quos!'
    }
])

</script>