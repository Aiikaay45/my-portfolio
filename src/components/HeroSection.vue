<script setup>
    import AOS from 'aos';
    import 'aos/dist/aos';
</script>
<template>
    <section class="relative w-full" data-aos="zoom-in-up" >
        <div class="absolute top-0 inset-x-0 h-64 flex items-start">
        <div class="h-24 w-2/3 bg-gradient-to-br from-[#570cac] blur-2xl invisible opacity-40"></div>
        <div class="h-20 w-3/5 bg-gradient-to-r from-[#670ccf] opacity-40 blur-2xl"></div>
        </div>
        <div class="w-full px-5 sm:px-8 md:px-12 lg:px-8 max-w-screen-lg lg:max-w-screen-xl mx-auto relative">
            <div class="grid lg:grid-cols-2 gap-10 xl:gap-14 relative pt-24 lg:max-w-none max-w-2xl md:max-w-3xl mx-auto">
                <div class="lg:py-6">
                    <div class="text-center lg:text-left">
                        <h1 class="pt-4 text-white font-bold text-4xl md:text-5xl lg:text-6xl">
                            Hi, I'm <span class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-pink-500">
                                Aiikaay
                            </span> 
                        </h1>
                    </div>
                    <p class="text-gray-300 pt-8 text-center lg:text-left mx-auto max-w-xl">
                        Lorem ipsum dolor sit amet, consectetur adipisicing elit. 
                        Repellendus numquam porro assumenda dolorum eveniet minima ex sed excepturi. 
                        Ab ex sed autem enim sit deserunt mollitia, atque officiis consequuntur necessitatibus.
                    </p>
                    <div class="flex items-center gap-3 pt-3 pt-9 flex-col sm:flex-row sm:w-max sm:mx-auto lg:mx-0">
                      <button class="px-6 md:px-7 py-3 rounded-full relative group w-full sm:w-max flex justify-center">
                        <span class="absolute inset-0 rounded-3xl group-hover:scale-105 origin-center transition-all ease-in-out bg-orange-400 border-2 border-transparent"></span>
                        <span class="relative flex items-center justify-center text-white">Hire Me</span>
                      </button>
                        <a
                            href="/resume.pdf"
                            download="resume.pdf"
                            class="border border-orange-400 px-6 md:px-7 py-3 rounded-full
                                    flex items-center gap-2 justify-center
                                    hover:scale-105 transition-all ease-in-out
                                    text-orange-400 w-full sm:w-max"
                            >
                            <svg
                                xmlns="http://www.w3.org/2000/svg"
                                viewBox="0 0 512 512"
                                fill="currentColor"
                                class="w-6 h-6"
                                aria-hidden="true"
                            >
                                <path d="M256,409.7,152.05,305.75,173.5,284.3l67.33,67.32V34h30.34V351.62L338.5,284.3,360,305.75ZM445.92,351v93.22a3.61,3.61,0,0,1-3.47,3.48H69.15a3.3,3.3,0,0,1-3.07-3.48V351H35.74v93.22A33.66,33.66,0,0,0,69.15,478h373.3a33.85,33.85,0,0,0,33.81-33.82V351Z" />
                            </svg>

                            <span>Download resume</span>
                            </a>
                    </div>
                </div>
                <div class="lg:h-full md:flex">
                <div class="flex w-full h-96 min-h-[24rem] lg:min-h-[none] lg:w-full items-center relative ">
                    <div class="absolute z-0 top-1/2 -translate-y-1/2 w-5/6 right-0 h-[calc(80%+20px)] bg-gradient-to-tr opacity-25 from-[#570cac] to-orange-400 blur-2xl"></div>
                    <div class="absolute h-full z-10 p-2 -translate-y-1/2 top-1/2 lg:right-3 md:right-40 sm:right-16 rounded-full shadow-lg border border-orange-400">
                        <img src="@/assets/top_boy.png" alt="Hero pic" width="500" loading="lazy"
                        class="w-full h-full rounded-full object-cover"
                        >
                    </div>
                </div>
        </div>

            </div>
        </div>
        
    </section>
</template>