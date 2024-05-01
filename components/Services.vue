<template>
    <section id="services" class="text-center">
        <h3>DIT BIED IK AAN</h3>
        <h2 class="mb-6">DIENSTEN</h2>
        <fieldset class="flex flex-wrap justify-center mb-10">
            <div v-for="(item, index) in serviceItems" :key="index" class="px-3 mb-3">
                <input
                    type="radio"
                    name="service"
                    :id="item.title"
                    :value="item.title"
                    v-model="checkedService"
                >
                <label :for="item.title" :class="['service-labels', { 'active': checkedService === item.title}]">{{ item.title }}</label>
            </div>
        </fieldset>
        <div class="flex justify-center">
            <img src="/assets/content/bubble.png" class="mr-14 bubble hidden lg:block">
            <div class="w-96 min-h-80 rounded-lg" id="service-container">
                <div class="p-7">
                    <h4 class="mb-2"><b>{{ selectedService.title }}</b></h4>
                    <p class="text-left mb-6">{{ selectedService.content }}</p>
                    <ul class="text-left pb-6 ml-3">
                        <li v-for="(item, index) in selectedService.pointers" :key="index" class="pointers">{{ item }}</li>
                    </ul>
                    <a href="#contact" class="contact-btn my-4 ml-3"><button class="contact-button">Neem contact op</button></a>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            serviceItems: [
                {
                    title: 'Wordpress of Wix',
                    content: 'Voor als je zelf alle touwtjes in handen wilt houden, bieden Wordpress en Wix een uitkomst! We maken een passend design, zetten de website op en zorgen ervoor dat je daarna zelf verder kunt. Natuurlijk kan ik je ook supporten met het onderhoud.',
                    pointers: ['Handige CMS voor al je content', 'Responsive & Accessible', 'Veel plugins, dus veel mogelijkheden', 'De touwtjes zelf in handen', 'Makkelijk in gebruik'],
                },
                {
                    title: 'Maatwerk website',
                    content: 'Als Wordpress of Wix niet zo interessant voor je is, omdat je bijvoorbeeld geen CMS nodig hebt, bouw ik een unieke, responsieve maatwerk-website voor je. Met Nuxt en Tailwind CSS maak ik creatieve websites die precies voldoen aan de wensen. Volledig customizable, maar dan een stuk lichter.',
                    pointers: ['Unieke website', 'Zo groot of zo klein als je maar wil'],
                },
                {
                    title: 'Developer Support',
                    content: 'Als gepassioneerde developer los ik graag vraagstukken op. Dus sta je voor een uitdaging die niets met websiteontwikkeling te maken heeft, bel me dan direct! Als je bijvoorbeeld een scriptje zoekt voor Zapier, of een stukje Javascript voor je nieuwsbrief, of voor langere tijd ondersteuning nodig hebt bij een project',
                    pointers: ['Korte klusjes', 'Langdurige projecten', 'Front-end', 'Scripts'],
                },
                {
                    title: 'Hosting',
                    content: 'Je wilt niet alleen een website, maar ook geen verdere zorgen over waar deze website dan staat. Of je hebt al een website en bent op zoek naar zorgeloze hosting? Ook dat kan ik voor je regelen met een bewust groenere hosting.',
                    pointers: ['Geen zorgen voor jou', 'Gekozen voor de groenere optie', 'Per maand of jaar', 'Snelle support'],
                },
                {
                    title: 'Domein',
                    content: 'Een domeinnaam registreren is zo gepiept. Kun je wat hulp daarbij gebruiken? Ik kan je advies geven over de partij en daarnaast je een helpende hand bieden tijdens de registratie. Ook als je je domeinnaam wilt verhuizen naar een nieuwe website.',
                    pointers: ['Betrouwbare registratie', 'Snel geregeld'],
                },
                {
                    title: 'Onderhoud',
                    content: 'Wanneer je bestaande website wel een update kan gebruiken, of je Wordpress-plugins achterlopen, je registraties bijna verlopen of je design wel een opfrisser kan gebruiken. Voor allerlei vormen van onderhoud ben ik beschikbaar.',
                    pointers: ['Ruim aanbod aan onderhoud', 'Eenmalig of maandelijks', 'Voor allerlei tools en technologie, zoals Wordpress, Google, Microsoft, hosting, domeinen en custom made websites.'],
                }
            ],
            checkedService: 'Wordpress of Wix'
        }
    },
    computed: {
        selectedService() {
            return this.serviceItems.find(item => item.title === this.checkedService);
        }
    }
}
</script>

<style scoped>
.pointers {
    list-style: disc;
}
</style>