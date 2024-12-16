<template>
    <section id="services-section">
        <a name="services"></a>
        <div class="content-container">
            <div class="mb-20">
                <h2>{{ sectionTitle }}</h2>
                <h3>{{ sectionSubTitle }}</h3>
            </div>
            <div class="flex mb-20">
                <div v-for="(item, index) in serviceItems" :key="index" id="service-item" class="w-full mr-4 p-4">
                    <h4 class="mt-2 mb-2">{{ item.title }}</h4>
                    <p class="mb-8">{{ item.content }}</p>
                </div>
            </div>
            <NuxtLink href="/website-maken" class="btn btn-secondary">{{ buttonText }}</NuxtLink>
        </div>
        <img src="/assets/content/dividers/waves/sand-to-blue/green-waves-one.svg" class="w-full">
    </section>
</template>

<script>
export default {
    data() {
        return {
            sectionTitle: 'Hé ondernemer met passie,',
            sectionSubTitle: 'om maar meteen met de deur in huis te vallen, dit is wat ik doe',
            buttonText: 'Lees meer over de websitediensten',
            serviceItems: [
                {
                    title: 'Web design & website',
                    content: 'Jouw unieke bedrijf verdient een one-of-a-kind online visitekaartje die past bij jou. Geen standaard thema\'s, maar samen rond de tafel brengen we jouw bedrijf tot leven online.',
                },
                {
                    title: 'Hosting & Support',
                    content: 'Op zoek naar betrouwbare hosting voor jouw website? Heb je een probleem met jouw huidige website? Met plezier verzorg ik jouw maandelijkse hosting, domeinnamen, e-mailproviders & allerlei soorten problemen!'
                },
                {
                    title: 'SEO-check',
                    content: 'Je hebt een toffe website, maar weet Google dat ook? Met de SEO-check zorg ik ervoor dat jouw website in de basis voor de SEO geoptimaliseerd is, zodat Google (en jouw publiek) jou kunnen vinden.'
                },
                {
                    title: 'Duurzaamcheck',
                    content: 'Of de \'duurzame website\' bestaat, is een discussie op zich. Maar met de duurzaamcheck kijken we hoe we jouw website iets energiezuiniger kunnen maken. Alle beetjes helpen, nietwaar?'
                },
            ]
        }
    }
}
</script>