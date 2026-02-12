<template>
    <section class="text-white mt-20">
        <div class="px-4 xl:pl-16">
            <div class="mb-4 md:flex md:justify-between xl:pr-16">
                <h2 class="text-4xl font-bold text-white">My Latest Project</h2>
                <div class="flex space-x-4 mb-4 mt-5 md:mt-0">
                    <button
                        v-for="category in ['all', 'web development', 'Mobile App']"
                        :key="category"
                        @click="setCategory(category)"
                        class="hover:text-orange-400"
                    >
                        {{ category }}
                    </button>
                </div>
            </div>
            <ul class="px-4 sm:py-16 xl:pr-16 grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 lg:grid-cols-3" data-aos="fade-right">
                <li 
                v-for="project in filteredProjects" :key="project.id">
                <div class="h-52 md:h-[24rem] rounded-t-xl relative overflow-hidden group"  
                >

                    <img 
                        :src="project.image"
                        alt="project image"
                        class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110" />

                    <!-- <div class="absolute inset-0 flex items-center justify-center bg-black/60 opacity-0 group-hover:opacity-100 transition-all duration-500">
                        <a
                        v-if="project.webURL" 
                        class="h-12 w-12 flex items-center justify-center border border-white rounded-full hover:bg-white hover:text-black transition" 
                        target="_blank"
                        :href="project.webURL">
                        </a>
                        
                        <a
                        v-if="project.gitURL" 
                        class="ml-4 h-12 w-12 flex items-center justify-center  border border-white rounded-full  hover:bg-white hover:text-black transition" 
                        target="_blank" 
                        :href="project.gitURL">
                        </a>
                    </div> -->
                </div>
                <div class="text-white rounded-b-xl mt-3 bg-[#111a3e] shadow-lg border-[#1f1641] py-6 px-4">
                    <h3 class="text-lg font-semibold uppercase lg:text-xl">{{ project.title }}</h3>
                    <p class="text-[#ADB7BE]">{{ project.description }}</p>
                    <div class="flex flex-wrap p-2.5">
                        <div v-for="technology in project.technologies" :key="technology" class="text-center ml-1 rounded-3xl bg-[#111827]"
                        style="box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1); border: 1px solid #111827;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur();"
                        >
                    <p class="px-2 py-1 text-sm text-white">
                        {{ technology }}
                    </p>
                    </div>
                    </div>
                </div>
                </li>
            </ul>
        </div>

    </section>
</template>
<script setup>
import { ref,computed } from 'vue'

 const Projects = ref([
    {
        id:1,
    category: 'web development',
    image: '/images/image_1.png',
    title: 'Project 1',
    description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Omnis maxime corrupti voluptatum cum nisi, qui sit quod reprehenderit aperiam accusamus magni perferendis aliquam a rem fugit nesciunt porro labore eaque.',
    technologies: ['vue.js 3','vuex','Express'],
    gitURL: '',
    webURL: ''
    },
    {
        id:2,
    category: 'Mobile App',
    image: '/images/image_2.png',
    title: 'Project 2',
    description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Omnis maxime corrupti voluptatum cum nisi, qui sit quod reprehenderit aperiam accusamus magni perferendis aliquam a rem fugit nesciunt porro labore eaque.',
    technologies: ['vue.js 3','vuex','Express'],
     gitURL: '',
    webURL: ''
    },
    {
        id:3,
    category: 'web development',
    image: '/images/image_3.png',
    title: 'Project 3',
    description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Omnis maxime corrupti voluptatum cum nisi, qui sit quod reprehenderit aperiam accusamus magni perferendis aliquam a rem fugit nesciunt porro labore eaque.',
    technologies: ['vue.js 3','vuex','Express'],
     gitURL: '',
    webURL: ''

    },
    {
        id:4,
    category: 'Mobile App',
    image: '/images/image_4.png',
    title: 'Project 4',
    description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Omnis maxime corrupti voluptatum cum nisi, qui sit quod reprehenderit aperiam accusamus magni perferendis aliquam a rem fugit nesciunt porro labore eaque.',
    technologies: ['vue.js 3','vuex','Express'],
     gitURL: '',
    webURL: ''
    },
    {
        id:5,
    category: 'web development',
    image: '/images/image_5.png',
    title: 'Project 5',
    description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Omnis maxime corrupti voluptatum cum nisi, qui sit quod reprehenderit aperiam accusamus magni perferendis aliquam a rem fugit nesciunt porro labore eaque.',
    technologies: ['vue.js 3','vuex','Express'],
     gitURL: '',
    webURL: ''
    },
    {
        id:6,
    category: 'web development',
    image: '/images/image_6.png',
    title: 'Project 6',
    description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Omnis maxime corrupti voluptatum cum nisi, qui sit quod reprehenderit aperiam accusamus magni perferendis aliquam a rem fugit nesciunt porro labore eaque.',
    technologies: ['vue.js 3','vuex','Express'],
     gitURL: '',
    webURL: ''
    },
 ])

const selectedCategory = ref('all')
const filteredProjects = computed(()=>{
    if(selectedCategory.value === 'all'){
        return Projects.value;
    }
    return Projects.value.filter(project => project.category.toLocaleLowerCase() == selectedCategory.value.toLocaleLowerCase());
})

const setCategory = (category) => {
  selectedCategory.value = category
}

</script>