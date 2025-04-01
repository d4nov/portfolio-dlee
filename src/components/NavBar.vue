<template>
    <header class="flex justify-between items-center p-3 pl-5 bg-opacity-50 relative z-20">
        <a href="" class="text-[#a5d8f1] text-2xl font-bold cursor-pointer">Dlee.</a>
        <!-- Mobile Toggle Button -->
        <div class="md:hidden z-30">
            <button type="button" 
                    class="block focus:outline-none"
                    @click="isMenuOpen = !isMenuOpen"
            >
                <span v-if="isMenuOpen" class="text-4xl">
                    <img src="https://img.icons8.com/ios-filled/100/a5d8f1/delete-sign.png" alt="close" width="40" height="40">
                </span>
                <span v-else class="text-4xl">
                    <img src="https://img.icons8.com/ios-filled/100/a5d8f1/menu--v6.png" alt="menu" width="40" height="40">
                </span>
            </button>
        </div>
        <!-- Navbar Link -->
        <nav
            :class="['fixed inset-0 z-20 flex flex-col items-center justify-center bg-[#342c5c] md:relative md:bg-transparent md:flex md:justify-between md:flex-row',
            isMenuOpen ? 'block' : 'hidden'
            ]"
        >
            <ul class="flex flex-col items-center space-y-5 md:flex-row md:space-x-5 md:space-y-0">
                <li v-for="item in Menu" :key="item.name">
                    <a :href="item.href" 
                       class="block text-[#a5d8f1] transition hover:text-[#b0fde0] ease-linear text-2xl md:text-lg"
                       @click="scrollToSection(item.href)"
                    >
                        {{ item.name }}
                    </a>
                </li>
            </ul>
            <div class="md:hidden">
                <p class="text-[#a5d8f1]">________________________</p>
            </div>
            <!-- Container cho các biểu tượng Facebook, Instagram và LinkedIn -->
            <div class="flex flex-row space-x-5 mt-5 md:mt-0 md:ml-5 ">
                <a href="https://facebook.com" target="_blank" class="block text-white transition hover:text-[#b0fde0] ease-linear text-2xl md:text-lg">
                    <img src="https://img.icons8.com/ios-filled/100/a5d8f1/facebook-new.png" alt="Facebook" width="30" height="30">
                </a>
                <a href="https://instagram.com" target="_blank" class="block text-white transition hover:text-[#b0fde0] ease-linear text-2xl md:text-lg">
                    <img src="https://img.icons8.com/ios-filled/100/a5d8f1/instagram-new.png" alt="Instagram" width="30" height="30">
                </a>
                <a href="https://linkedin.com" target="_blank" class="block text-white transition hover:text-[#b0fde0] ease-linear text-2xl md:text-lg">
                    <img src="https://img.icons8.com/ios-filled/100/a5d8f1/linkedin.png" alt="LinkedIn" width="30" height="30">
                </a>
                
            </div>
            <!-- Container cho biểu tượng điện thoại (chỉ hiển thị trên mobile) -->
            <div class=" md:hidden flex flex-row space-x-5 mt-5">
                <a href="tel:+84772101544" class=" text-[#a5d8f1] transition hover:text-[#a5d8f1] ease-linear text-2xl md:text-lg flex items-center space-x-2">
                    <img src="https://img.icons8.com/ios-filled/100/a5d8f1/phone.png" alt="Telephone" width="24" height="24">
                    <span>(+84) 772 101 544</span>
                </a>
            </div>
            <div class="md:hidden flex flex-row space-x-5 mt-5">
    <a href="mailto:lmduc.2k1@gmail.com" class="flex items-center transition hover:text-[#b0fde0] ease-linear">
        <img src="https://img.icons8.com/ios-filled/100/a5d8f1/gmail.png" alt="Gmail" width="24" height="24" class="mr-2">
        <span class="text-[#a5d8f1]">lmduc.2k1@gmail.com</span>
    </a>
</div>
        </nav>
    </header>
</template>

<script setup>
import { ref } from 'vue';

const Menu = ref([
    { name: 'Skills', href: '#services' },
    { name: 'Experience', href: '#experience' },
    { name: 'Projects', href: '#projects' },
    { name: 'Contact', href: '#contact' },
]);

const isMenuOpen = ref(false);

const scrollToSection = (href) => {
    isMenuOpen.value = false;
    const section = document.querySelector(href);
    if (section) {
        section.scrollIntoView({ behavior: 'smooth' });
    }
}
</script>