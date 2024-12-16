<template>
    <nav>
        <ul class="flex p-4 justify-end items-center">
            <li v-for="(item, index) in navItems" :key="index" class="p-2 mr-4">
                <a v-if="item.button" href="/#contact" class="btn btn-secondary">{{ item.title }}</a>
                <NuxtLink v-else :to="item.url">{{ item.title }}</NuxtLink>
            </li>
        </ul>
    </nav>
</template>

<script>
export default {
    data() {
        return {
            navItems: [
                {
                    title: 'Thuis',
                    url: '/'
                },
                {
                    title: 'Website!',
                    url: '/website-maken'
                },
                {
                    title: 'Wie?',
                    url: 'over'
                },
                {
                    title: 'Contact',
                    button: true,
                }
            ]
        }
    }
}
</script>