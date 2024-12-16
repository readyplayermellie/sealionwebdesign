<template>
    <section id="advantages-section">
        <div class="content-container">
            <div class="mb-20">
                <h3>{{ subtitle }}</h3>
                <h2>{{ title }}</h2>
            </div>
            <div class="flex flex-wrap mb-20">
                <div v-for="(item, index) in advantageItems" :key="index" id="advantage-item" class="w-1/4 mr-4 p-4 mb-4">
                    <h4 class="mt-2 mb-2">{{ item.title }}</h4>
                    <p class="mb-4">{{ item.content }}</p>
                </div>
            </div>
            <a href="#contact" class="btn btn-tertiary">{{ buttonText }}</a>
        </div>
        <img src="~/assets/content/dividers/waves/Pink-to-blue/blue-waves-one.svg" class="w-full">
    </section>
</template>

<script>
export default {
    data() {
        return {
            title: 'Daarom zijn al mijn websites',
            subtitle: 'I love websites maken voor ondernemers zoals jij',
            buttonText: 'Neem contact op',
            advantageItems: [
                {
                    title: 'Uniek',
                    content: 'Van moodboard tot uiteindelijk resultaat: Mijn websites zijn op maat gemaakt en uniek voor elke gepassioneerde ondernemer.'
                },
                {
                    title: 'Responsief',
                    content: 'Of jouw favoriete publiek nu op een laptop, tablet of telefoon naar jouw website gaat: Elk formaat werkt perfect.'
                },
                {
                    title: 'Toegankelijk',
                    content: 'Elke website moet voor zoveel mogelijk mensen te bezoeken zijn. Daarom hou ik me in het design aan de WCAG 2.2 richtlijnen voor toegankelijkheid van websites. Wel zo sociaal.'
                },
                {
                    title: 'Duurzamer',
                    content: 'Ik vertaal dit als: Alleen gebruiken wat we écht nodig hebben (dus niet alleen maar Wordpress), kiezen voor een duurzamere hostingpartij en energiezuinige keuzes maken.'
                },
                {
                    title: 'Gestructureerd',
                    content: 'Niet alleen de websitestructuur zit snor. Ook mijn websiteproces is helder en duidelijk, zodat je altijd weet wanneer je wat van me mag verwachten - en wanneer je zelf aan de slag kunt.'
                },
                {
                    title: 'Vol passie',
                    content: 'Websites maken voor ondernemers met een passie voor hun werk vind ik ontzettend inspirerend en daarom vind je in elke website die ik maak een stukje passie.'
                }
            ]
        }
    }
}
</script>