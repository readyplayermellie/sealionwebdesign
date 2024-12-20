<template>
    <section id="package-section">
        <div class="content-container">
            <div class="mb-16">
                <h3>{{ subtitle }}</h3>
                <h2>{{ title }}</h2>
            </div>
            <div class="flex mb-12">
                <div v-for="(item, index) in packageItems" :key="index" id="service-item" class="w-full mr-4 p-4 package-item">
                    <h4 class="mt-2 mb-2">{{ item.title }}</h4>
                    <p>{{ item.subtitle }}</p>
                    <ul class="ml-5 pt-4 pb-4">
                        <li v-for="(point, index) in item.specifics" :key="index">{{ point }}</li>
                    </ul>
                    <p class="mb-8 bold-text">Vanaf {{ item.price }}</p>
                </div>
            </div>
            <a href="/#contact" class="btn btn-primary">{{ buttonText }}</a>
        </div>
        <img src="~/assets/content/dividers/waves/Blue-to-pink/pink-waves-one.svg" class="w-full">
    </section>
</template>

<script>
export default {
    data() {
        return {
            title: 'Wat mag dat kosten dan?',
            subtitle: 'Pakketten voor jouw website en alles daaromheen',
            buttonText: 'Vraag een vrijblijvende offerte aan',
            packageItems: [
                {
                    title: 'Web design & website',
                    subtitle: 'Uniek en op maatgemaakt - pakketprijs',
                    specifics: ['Uniek design', '1 tot oneindig pagina\'s', 'Wordpress, Wix of zonder platform', 'SEO-check', 'Duurzaamcheck', 'Vanaf oplevering na 1 maand'],
                    price: '1200'
                },
                {
                    title: 'Hosting & Support',
                    subtitle: 'Kom maar op met die problemen - eenmalig of maandelijks',
                    specifics: ['Duurzamere hostingprovider', 'Thema & plugin updates', 'Meedenken met jouw ideeën', 'E-mailproblemen', 'Domeinnaam regelen', 'Gebroken website fixen'],
                    price: '50'
                },
                {
                    title: 'SEO-check',
                    subtitle: 'Zodat Google jouw publiek naar je stuurt - eenmalig',
                    specifics: ['Zoekwoordenonderzoek in jouw niche', 'Contentadvies', 'Advies met verbeterpunten', 'Vanaf 2 uur'],
                    price: '65 per uur'
                },
                {
                    title: 'Duurzaamcheck',
                    subtitle: 'Zoveel hebben we toch niet nodig - eenmalig',
                    specifics: ['Hoe duurzaam is de website nu?', 'Advies met verbeterpunten', 'Implementatie van de verbeteringen', 'Energieverbruiksbanner', 'Vanaf 2 uur'],
                    price: '65 per uur'
                },
            ]
        }
    }
}
</script>