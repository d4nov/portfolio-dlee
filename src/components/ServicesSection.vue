<template>
    <section class="text-white mt-20" id="services">
        <div class="px-4 xl:pl-16">
            <h2 class="text-4xl font-bold text-white mb-4">Skills</h2>
        </div>
        <div class="py-8 xl:px-16 px-4 sm:py-16 grid grid-cols-2 gap-6 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 lg:grid-cols-6">
            <a 
                v-for="service in services" 
                :key="service.id" 
                :href="service.link" 
                target="_blank" 
                class="block"
            >
                <div 
                    data-aos="fade-up"
                    class="px-3 py-4 rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] transition-all duration-300 ease-in-out transform hover:scale-105 hover:shadow-2xl hover:border-primary"
                >
                    <div class="mx-auto h-24 w-24 text-center xl:h-28 xl:w-28">
                        <div>
                            <img :src="service.icon" alt="service icon" class="w-full h-full object-contain">
                        </div>
                    </div>
                    <div class="text-center">
                        <h3 class="pt-5 text-lg font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary lg:text-xl">
                            {{ service.name }}
                        </h3>
                    </div>
                </div>
            </a>
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue';

const services = ref([
    {
        id: 1,
        icon: '/images/js.png',
        name: 'JavaScript',
        link: 'https://developer.mozilla.org/en-US/docs/Web/JavaScript' // Link tương ứng
    },
    {
        id: 2,
        icon: '/images/ts.png',
        name: 'TypeScript',
        link: 'https://www.typescriptlang.org/' // Link tương ứng
    },
    {
        id: 3,
        icon: '/images/science.png',
        name: 'React JS',
        link: 'https://reactjs.org/' // Link tương ứng
    },
    {
        id: 4,
        icon: '/images/vue.png',
        name: 'Vue JS',
        link: 'https://vuejs.org/' // Link tương ứng
    },
    {
        id: 8,
        icon: '/images/tailwind-css.svg',
        name: 'Tailwind CSS',
        link: 'https://tailwindcss.com/' // Link tương ứng
    },
    {
        id: 9,
        icon: '/images/git.png',
        name: 'Git',
        link: 'https://git-scm.com/' // Link tương ứng
    },
    // {
    //     id: 10,
    //     icon: '/images/dif.png',
    //     name: 'More...',
    //     link: '#' // Link tương ứng (có thể thay đổi)
    // },
]);
</script>