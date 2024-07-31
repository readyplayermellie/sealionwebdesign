<template>
    <header class="w-full">
        <nav class="flex justify-between items-center lg:px-10 px-5">
            <span><img src="/assets/content/logo-volledig.png" class="h-12"></span>
            <ul class="flex items-center">
                <li v-for="(item, index) in navItems" :key="index" class="px-3 hidden md:inline"><a :href="item.link">{{ item.text }}</a></li>
                <a :href="btn.link" class="contact-btn my-4 ml-3"><button class="contact-button">{{ btn.text }}</button></a>
            </ul>
        </nav>
        <div id="header-content">
            <h1>{{ title }}</h1>
            <h2>{{ subtitle }}</h2>
        </div>
    </header>
</template>

<script>
export default {
    data() {
        return {
            title: 'Sea Lion Web Design',
            subtitle: 'Creatieve webontwikkeling die indruk maakt en impact heeft',
            navItems: [
                {
                    text: 'Website',
                    link: '#intro'
                },
                {
                    text: 'Diensten',
                    link: '#services'
                },
                {
                    text: 'Over',
                    link: '#about'
                },
            ],
            btn: {
                text: 'CONTACT',
                link: '#contact'
            }
        }
    }
}
</script>