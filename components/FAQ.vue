<template>
    <section class="mt-40 mb-40">
        <a name="faq"></a>
        <div class="container">
            <h2 class="pb-8 text-3xl border-b border-white">{{ title }}</h2>
            <div v-for="(item, index) in accordionList" :key="index" class="border-b border-white">
                <div>
                    <a href="javascript:void(0);" @click="accordionHandler(index)" class="flex justify-between w-full pt-4 pb-4">
                        <h3>{{ item.question }}</h3>
                        <img
                            src="../assets/icons/clam.png"
                            alt="Sluit de accordion door te klikken op dit icoon"
                            class="w-8 h-8"
                            :id="`clam-closed-${index}`"
                        >
                        <img
                            src="../assets/icons/clam-open.png"
                            alt="Sluit de accordion door te klikken op dit icoon"
                            class="w-8 h-8 hidden"
                            :id="`clam-open-${index}`"
                        >
                    </a>
                </div>
                <div class="hidden pb-8" :id="item.id">
                    <p class="pr-8">{{ item.answer }} <a :href="item.url" class="hover:underline hover:underline-offset-4">{{ item.linkText }}</a></p>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            title: 'Veelgestelde vragen',
            accordionList: [
                {
                    question: 'Wat kost het om een professionele website te laten maken?',
                    answer: 'De kosten van een website zijn afhankelijk van jouw wensen. Bij Sea Lion Web Design beginnen de pakketten voor een volledig nieuwe website bij 1249,- incl. BTW. Heb je al een toffe website, maar kan deze wel een opfrisser gebruiken? Dit kan al vanaf 499,- inclusief BTW.',
                    id: 'question-one',
                    linkText: 'Meer over de prijzen en pakketten vind je hier.',
                    url: '/#prijzen'
                },
                {
                    question: 'Hoe lang duurt het om een nieuwe professionele website te bouwen?',
                    answer: 'Evenals de prijs van een professionele website is de tijd tussen de intake en de oplevering van een nieuwe website afhankelijk van jouw wensen. De minimale doorlooptijd voor een nieuwe website bij Sea Lion Web Design is 6 weken. Zo nemen we genoeg tijd voor jouw wensen, de content, het design en de implementatie. Staat jouw nieuwe website liever vandaag dan morgen? Als het in de agenda past, kunnen we jouw nieuwe website ook met spoed neerzetten.',
                    id: 'question-two',
                    linkText: 'Informeer hier naar de mogelijkheden.',
                    url: '/#contact'
                },
                {
                    question: 'Wat zijn de voordelen van een maatwerk website?',
                    answer: 'Alle designs van Sea Lion Web Design zijn uniek en op maat gemaakt, omdat ik ervaar dat de standaard thema’s vaak niet toereikend genoeg voor het doel van de website zijn en te wensen overlaten. Met maatwerk websites heb je alle touwtjes zelf in handen en kan het design volledig toegespitst worden op jouw doelgroep, merk en bedrijf. Zo zorgen we ervoor dat jouw unieke website perfect past bij jouw unieke bedrijf.',
                    id: 'question-three',
                    linkText: 'Benieuwd of we jouw wensen tot leven kunnen brengen?',
                    url: '/#contact'
                },
                {
                    question: 'Kan ik mijn website zelf beheren nadat deze is gebouwd?',
                    answer: 'Ja zeker! Als je zelf de website wil beheren maken we samen een website met gebruiksvriendelijke platforms als Wordpress of Wix. Zo ben je in control over de content van jouw website. Ook de hosting kun je zelf regelen. Natuurlijk kun je bij me aankloppen als je wat hulp bij jouw website kan gebruiken. Als je de touwtjes liever uit handen geeft, zorg ik ervoor dat jouw website up-to-date blijft en houd ik de aanpassingen bij. Wel zo makkelijk.',
                    id: 'question-four'
                },
                {
                    question: 'Wat is inbegrepen bij de website-pakketten?',
                    answer: 'De website-pakketten bestaan uit alles wat jij nodig hebt om jouw bedrijf online goed neer te zetten. Van een uniek design en ontwikkeling tot de hosting en technische support. De SEO (online vindbaarheid) van jouw website zet ik in de basis goed neer en ik check direct even hoe duurzaam jouw website is en of we dit nog kunnen verbeteren. Natuurlijk vergeet ik de domeinnaam niet en indien je dat wil, zet ik gepersonaliseerde e-mailadressen voor je op. Zo kunnen jouw klanten jou altijd vinden én bereiken.',
                    id: 'question-five',
                    linkText: 'Bekijk de website-pakketten hier.',
                    url: '/#prijzen'
                },
                {
                    question: 'Hoe zorg ik ervoor dat ik goed gevonden wordt door Google?',
                    answer: 'Een brede vraag, maar in de basis betekent dit dat jij met jouw website aan Google laat zien dat jij een expert bent binnen jouw vakgebied. Op technisch gebied heeft jouw website snelle laadtijden, een mobielvriendelijk design en relevante content die jouw klanten (en Google) van alle informatie voorziet die zij nodig hebben. SEO-optimalisatie zorgt voor een goede basis in vindbaarheid voor jouw website en is inbegrepen bij alle website-pakketten.',
                    id: 'question-six'
                },
                {
                    question: 'Waarom zou ik kiezen voor Sea Lion Web Design?',
                    answer: 'Ik hou van websites maken en daarom heb ik gepassioneerde ondernemers met toffe bedrijven zoals jij graag met mijn passie aan een goed vindbare, toegankelijke website. Samen duiken we in jouw wensen en ideeën en met persoonlijke aandacht, transparante prijzen en oog voor detail breng ik jouw professionele website tot leven. Neem contact op voor jouw gratis 30-minuten intake!',
                    id: 'question-seven',
                    linkText: 'Neem contact op voor jouw gratis 30-minuten intake!',
                    url: '/#contact'
                }
            ]
        }
    },
    methods: {
        accordionHandler(i) {
            this.accordionList.forEach((item) => {
                if (i === this.accordionList.indexOf(item)) {
                    const selectedQuestion = document.getElementById(item.id);
                    const openedClam = document.getElementById(`clam-open-${i}`);
                    const closedClam = document.getElementById(`clam-closed-${i}`);

                    if (selectedQuestion.style.display === 'block') {
                        selectedQuestion.style.display = 'none';
                        openedClam.style.display = 'none';
                        closedClam.style.display = 'block';
                    } else {
                        selectedQuestion.style.display = 'block';
                        openedClam.style.display = 'block';
                        closedClam.style.display = 'none';
                    }
                }
            });
        }
    }
}
</script>