<template>
    <section class="pt-40 pb-40" id="package-section">
        <a name="prijzen"></a>
        <div class="container">
            <div class="pb-4">
                <h2 class="pb-4 text-3xl">{{ title }}</h2>
                <p class="pb-4">{{ subtitle }}</p>
            </div>
            <div class="flex w-full flex-wrap">
                <div v-for="(item, index) in packageContent" :key="index" class="border border-white p-4 w-full sm:w-1/4 sm:m-0 min-w-52">
                    <h3 class="text-xl mb-4 pb-2 mt-8 border-b border-white">{{ item.title }}</h3>
                    <p class="mb-2">{{ item.content }}</p>
                    <ul class="mb-4 pb-2 border-b border-white h-40">
                        <li v-for="(i, index) in item.list" :key="index" class="package-items text-sm">{{ i }}</li>
                    </ul>
                    <p class="mb-8">Vanaf <span class="text-xl font-bold">{{ item.price }}</span></p>
                    <NuxtLink to="#contact" class="btn btn-primary block text-center w-full">{{ item.buttonText }}</NuxtLink>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            title: 'Prijzen & pakketten',
            subtitle: 'Goed om te weten: De genoemde prijzen zijn inclusief BTW. Ik hanteer 3 betaaltermijnen, namelijk bij acceptatie offerte, acceptatie design en oplevering.',
            packageContent: [
                {
                    title: 'Webdesign & ontwikkeling',
                    content: 'In dit pakket zit standaard:',
                    list: [
                        'Uniek design', 
                        '1 tot oneindig pagina\'s',
                        'Wordpress, Wix of zonder platform',
                        'SEO-check',
                        'Duurzaam-check', 
                        'Vanaf oplevering na 6 weken'
                    ],
                    price: '1295',
                    buttonText: 'Boek een gratis intake'
                },
                {
                    title: 'Hosting en technische support',
                    content: 'Als je hulp nodig hebt bij:',
                    list: [
                        'Duurzamere hostingprovider',
                        'Thema & plugin updates',
                        'Meedenken met jouw ideeën',
                        'E-mailproblemen',
                        'Domeinnaam regelen',
                        'Gebroken website fixen'
                    ],
                    price: '50',
                    buttonText: 'Schakel me in'
                },
                {
                    title: 'Kan-Google-me-vinden-SEO-check',
                    content: 'In dit pakket zit standaard:',
                    list: [
                        'Zoekwoordenonderzoek in jouw niche',
                        'Contentadvies',
                        'Advies met verbeterpunten'
                    ],
                    price: '199',
                    buttonText: 'Vraag meer info aan'
                },
                {
                    title: 'Is-mijn-website-duurzaam-check',
                    content: 'In dit pakket zit standaard:',
                    list: [
                        'Advies met verbeterpunten',
                        'Implementatie van de verbeteringen',
                        'Energieverbruiksbanner'
                    ],
                    price: '199',
                    buttonText: 'Vraag meer info aan'
                }
            ]
        }
    },
}
</script>