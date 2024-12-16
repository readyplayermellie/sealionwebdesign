<template>
    <section id="intro-section">
        <div class="content-container flex justify-center">
            <div>
                <h2>{{ sectionTitle }}</h2>
                <p v-for="(item, index) in sectionContent" :key="index" class="mt-4 leading-loose">{{ item }}</p>
            </div>
        <img src="/assets/content/decoration/jellyfish-pink.png" id="jelly-img">
        </div>
        <img src="/assets/content/dividers/waves/blue-to-pink/pink-waves-one.svg" class="w-full">
    </section>
</template>

<script>
export default {
    data() {
        return {
            sectionTitle: 'Maar waarom doe ik dit eigenlijk?',
            sectionContent: [
                'Omdat ik een passie heb voor de online aanwezigheid van jouw bedrijf dat je met passie leidt.', 
                'Mijn hart gaat sneller kloppen van een zakelijke website die me direct de ondernemer erachter laat zien en me vertelt  wat ik wil weten. Een heldere navigatie, aantrekkelijke foto\’s en vooral een makkelijke én toegankelijke flow die jouw klant meeneemt op een reis door jouw bedrijf.'
            ]
        }
    }
}
</script>