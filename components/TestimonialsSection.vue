<template>
    <section class="pt-40 pb-40">
        <a name="reviews"></a>
        <div class="container">
            <h2 class="pb-4 text-3xl">{{ title }}</h2>
            <div v-for="(item, index) in testimonialItems" :key="index" class="flex mt-8">
                <img :src="item.icon" alt="Decoratief icoon bij een review van een klant" class="h-12 w-12">
                <p class="ml-8">{{ item.content }}</p>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            title: 'Lovende woorden van happy ondernemers',
            testimonialItems: [
                {
                    icon: '/icons/fish.png',
                    content: '“Melanie is nauwkeurig en precies waardoor ik het vertrouwen heb dat ik ontzorgd wordt.” - De Bouwdirigent'
                },
                {
                    icon: '/icons/squid.png',
                    content: '“Melanie’s doorzettingsvermogen en haar meedenkende dienstverlening zorgen er voor dat ik het iedereen kan aanraden om met Sea Lion Web Design in zee te gaan!” - Joost'
                },
                {
                    icon: '/icons/octopus.png',
                    content: '“Ik beveel Melanie ten zeerste aan voor iedereen die klaar is om de volgende stap te zetten, maar vastloopt op het gebied van webdesign en online vindbaarheid.” - De Bouwdirigent'
                }
            ]
        }
    }
}
</script>