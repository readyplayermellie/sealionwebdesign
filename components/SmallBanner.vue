<template>
    <div class="border-b border-t border-white overflow-visible">
        <ul class="flex list-none justify-center flex-wrap" id="scrolling-banner">
            <li v-for="(item, index) in list" :key="index" class="p-2 pr-8 banner-items">{{ item.title }}</li>
        </ul>
    </div>
</template>

<script>
export default {
    data() {
        return {
            list: [
                { title: 'Web Design' },
                { title: 'Website Ontwikkeling' },
                { title: 'Hosting' },
                { title: 'Technische Support' },
                { title: 'SEO Optimalisatie' },
                { title: 'Duurzame Website' },
                { title: 'Front-end Developer' }
            ]
        }
    }
}
</script>