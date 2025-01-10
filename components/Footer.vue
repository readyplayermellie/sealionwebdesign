<template>
    <footer class="container">
        <div class="md:flex justify-between pb-8 pt-8">
            <div class="md:w-1/3 pb-4">
                <h3 class="text-xl">{{ text.title }}</h3>
                <p>{{ text.content }}</p>
                <div class="flex pt-2">
                    <a href="https://www.instagram.com/sealionwebdesign" target="_blank">
                        <img src="../public/icons/instagram.png" alt="Link naar instagrampagina van Sea Lion Web Design" class="h-6 w-6 mr-2">
                    </a>
                    <a href="https://www.linkedin.com/in/melaniedeleeuw/" target="_blank">
                        <img src="../public/icons/linkedin.png" alt="Link naar linkedinpagina van Sea Lion Web Design" class="h-6 w-6">
                    </a>
                </div>
            </div>
            <div class="pb-4">
                <h3 class="text-xl">{{ contactDetails.title }}</h3>
                <ul>
                    <li v-for="(item, index) in contactDetails.list" :key="index" class="list-disc list-inside">{{ item }}</li>
                </ul>
            </div>
            <div>
                <h3 class="text-xl">{{ importantLinks.title }}</h3>
                <ul>
                    <li v-for="(item, index) in importantLinks.list" :key="index" class="list-disc list-inside">{{ item }}</li>
                </ul>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    data() {
        return {
            title: 'Neem contact met me op',
            subtitle: 'Zodat wij morgen al aan jouw nieuwe professionele website kunnen werken.',
            content: [
                'In een gratis intake die 30 minuten duurt, vertel jij mij wat je zoekt en kijk ik samen met jou naar de mogelijkheden.',
                'Staat jouw wens niet op de website? Ook dan krijg ik graag jouw bericht. Ik hou van uitdagingen!',
            ],
            text: {
                title: 'De koffie staat klaar',
                content: 'En de virtuele potloden zijn geslepen om samen met jou een mooie, unieke website neer te zetten. Zo’n website waar je over op wil scheppen.',
            },
            contactDetails: {
                title: 'Contactgegevens',
                list: [
                    'Bedrijfsnaam: Sea Lion Web Design',
                    'Websitebouwer: Melanie de Leeuw',
                    'E-mail: Hello@sealionwebdesign.com',
                    'Locatie: Diemen, Nederland',
                    'Kvk: 92265197'
                ]
            },
            importantLinks: {
                title: 'Wat ik doe',
                list: [
                    'Web design',
                    'Website ontwikkeling',
                    'SEO-optimalisatie',
                    'Website verduurzaming',
                ]
            }
        }
    }
}
</script>