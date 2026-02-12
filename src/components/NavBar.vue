<script setup>
    import { ref } from 'vue';
    const Menu =ref([
        {name: 'Services',href: '#services'},
        {name: 'About Me',href: '#about'},
        {name: 'Skills',href: '#skills'},
        {name: 'Projects',href: '#projects'},
        {name: 'Testimonials',href: '#testimonials'},
        {name: 'Contact',href: '#contact'},
    ])

    const isMenuOpen =ref(false)
    const scrollToSection =(href)=>{
        isMenuOpen.value=false;
        const section=document.querySelector(href);
        if(section){
            section.scrollIntoView({behavior : 'smooth'});
        }
    }
</script>

<template>
    <header class="flex justify-between items-center p-6 bg-opacity-50 relative z-20">
        <div class="text-white text-3xl font-bold">LOGO</div>
        <!--Mobile Toggle Button-->
        <button type="button" 
        class="block md:hidden focus:outline-none"
        @click="isMenuOpen = !isMenuOpen"
        >
            <span v-if="isMenuOpen" class="text-5xl">
            <img src="//img.icons8.com/?size=100&id=8112&format=png&color=000000" alt="close" width="50" height="50">
            </span>
            <span v-else class="text-5xl">
                <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <path d="M4 6H20M4 12H20M4 18H20" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path> </g></svg>            </span>
        </button>
        <!--Navbar link-->  
        <nav 
        :class="['fixed inset-0 z-20 flex items-center justify-center bg-[#111827] md:relative md:bg-transparent', 
        isMenuOpen ? 'block' : 'hidden md:block'
        ]"
        >
            <ul class="flex flex-col items-center space-y-5  md:flex-row md:space-x-8 md:space-y-0">
                <li v-for="item in Menu" :key="item.name">
                    <a :href="item.href"
                    class="text-white text-2xl md:text-lg hover:text-primary transition"
                    @click.prevent="scrollToSection(item.href)"
                    >
                        {{ item.name }}  
                </a>

                </li>
                </ul>
        </nav>
    </header>
</template>
