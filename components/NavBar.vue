<template>
    <nav class="p-8 flex justify-end w-full">
        <ul class="lg:hidden">
            <li class="relative"><img src="../assets/icons/hamburger.png" alt="Open mobiel menu" class="w-8 h-8 relative">
                <ul class="absolute w-72" id="dropdown-menu">
                    <li v-for="(item, index) in navList" :key="index">
                        <a :href="item.url" class="p-4 w-72 block">{{ item.title }}</a>
                    </li>
                </ul>
            </li>
        </ul>
        <!-- <div id="desktop-menu" class="hidden lg:block">
            <a v-for="(item, index) in navList" :key="index" v-if="item.iconSrc" :href="item.url" class="m-4 pb-2 hover:border-b">
                <img :src="item.iconSrc" :alt="item.iconAlt">
            </a>
            <a else v-for="(item, index) in navList" :key="index" :href="item.url" class="m-4 pb-2 hover:border-b">{{ item.title }}</a>
        </div> -->
        <ul id="desktop-menu" class="hidden lg:flex">
            <li v-for="(item, index) in navList">
                <a v-if="item.iconSrc" :key="index" :href="item.url" class="p-0">
                    <img :src="item.iconSrc" :alt="item.iconAlt" class="h-6 w-6 mr-4">
                </a>
                <a else :key="index" :href="item.url" class="m-4 pb-2 hover:border-b">{{ item.title }}</a>
            </li>
        </ul>
    </nav>
</template>

<script>
export default {
    data() {
        return {
            navList: [
                {
                    iconSrc: 'icons/sailboat.png',
                    iconAlt: 'Icoon van een zeilboot als link voor de homepagina',
                    url: '/',
                },
                {
                    title: 'Diensten',
                    url: '/#diensten',
                },
                {
                    title: 'Reviews',
                    url: '/#reviews',
                },
                {
                    title: 'Prijzen en pakketten',
                    url: '/#prijzen',
                },
                {
                    title: 'Veelgestelde vragen',
                    url: '/#faq',
                },
                {
                    title: 'Contact',
                    url: '/#contact'
                }
            ]
        }
    },
    methods: {
        openMobileMenu() {
            const mobileMenuContainer = document.getElementById('mobile-menu');
            mobileMenuContainer.classList.contains('closed')
                ? mobileMenuContainer.classList.remove('closed')
                : mobileMenuContainer.classList.add('closed');
        }
    }
}
</script>