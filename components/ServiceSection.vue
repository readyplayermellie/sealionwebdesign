<template>
    <section class="pt-4 pb-4 lg:flex lg:justify-end" id="service-section">
        <a name="diensten"></a>
        <div class="container lg:w-1/2" id="service-container">
            <h2 class="pb-4 text-3xl">{{ title }}</h2>
            <div>
                <div v-for="(item, index) in serviceItems" :key="index" class="border border-white p-4 lg:max-w-lg">
                    <h3 class="text-xl mb-2">{{ item.title }}</h3>
                    <p>{{ item.content }}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            title: 'Diensten',
            serviceItems: [
                {
                    title: 'Webdesign en websiteontwikkeling',
                    content: 'Jouw unieke bedrijf verdient een one-of-a-kind online visitekaartje die past bij jou. Geen standaard thema\'s, maar samen rond de tafel brengen we jouw bedrijf tot leven online.'
                },
                {
                    title: 'Hosting en technische support',
                    content: 'Op zoek naar betrouwbare hosting voor jouw website? Heb je een probleem met jouw huidige website? Met plezier verzorg ik jouw maandelijkse hosting, domeinnamen, e-mailproviders & allerlei soorten problemen!'
                },
                {
                    title: 'De Kan-Google-me-vinden-SEO-check',
                    content: 'Je hebt een toffe website, maar weet Google dat ook? Met de SEO-check zorg ik ervoor dat jouw website in de basis voor de SEO geoptimaliseerd is, zodat Google (en jouw publiek) jou kunnen vinden.'
                },
                {
                    title: 'De Is-mijn-website-duurzaam-check',
                    content: 'Met de duurzaamcheck kijken we hoe we jouw website iets energiezuiniger kunnen maken én we zorgen ervoor dat we enkel gebruiken wat we echt nodig hebben. Alle beetjes helpen.'
                }
            ]
        }
    }
}
</script>