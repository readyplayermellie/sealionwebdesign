<template>
    <div>
        <div class="mb-2 w-1/3 pr-24">
            <h4 class="pb-2">{{ outroText.title }}</h4>
            <p>{{ outroText.content }}</p>
        </div>
        <div class="mb-2">
            <h4 class="pb-2">{{ contactInfo.title }}</h4>
            <div v-for="(item, index) in contactInfo.content" :key="index">
                <NuxtLink v-if="item.url" :to="item.url" class="underline underline-offset-2">{{ item.title }}</NuxtLink>
                <span v-else>{{ item.title }}</span>
            </div>
        </div>
        <div class="mb-2">
            <h4 class="pb-2">{{ sitemap.title }}</h4>
            <div v-for="(item, index) in sitemap.content" :key="index">
                <NuxtLink v-if="item.url" :to="item.url" class="underline underline-offset-2">{{ item.title }}</NuxtLink>
                <span v-else>{{ item.title }}</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            outroText: {
                title: 'De koffie staat klaar',
                content: 'en de virtuele potloden zijn geslepen om samen met jou een mooie, unieke website neer te zetten. Zo’n website waar je over op wil scheppen.'
            },
            contactInfo: {
                title: 'Sea Lion Web Design',
                content: [
                    {
                        title: 'Melanie de Leeuw',
                    },
                    {
                        title: '+31 6 133 456 99',
                    },
                    {
                        title: 'hello@sealionwebdesign.com',
                        url: 'mailto:hello@sealionwebdesign.com'
                    },
                    {
                        title: 'KvK: 92265197',
                    },
                    {
                        title: 'Meer over mij',
                        url: '/over'
                    },
                ]
            },
            sitemap: {
                title: 'Belangrijke links',
                content: [
                    {
                        title: 'Website nodig?',
                        url: '/website-maken'
                    },
                    {
                        title: 'Uniek websitedesign',
                        url: '/website-maken'
                    },
                    {
                        title: 'Hosting & Support',
                        url: '/website-maken'
                    },
                    // {
                    //     title: 'Algemene voorwaarden',
                    //     url: '/algemene-voorwaarden'
                    // },
                    // {
                    //     title: 'Privacyverklaring',
                    //     url: '/privacy'
                    // },
                ]
            },
        }
    }
}
</script>