<template>
    <section id="more-advantages-section">
        <div class="content-container">
            <div class="mb-20">
                <h3>{{ subtitle }}</h3>
                <h2>{{ title }}</h2>
            </div>
            <div class="flex mb-20">
                <img src="../assets/content/decoration/seal.jpg" class="rounded-lg w-1/3">
                <p class="pl-4">{{ content }}</p>
            </div>
        </div>
        <img src="../assets/content/dividers/waves/Sand-to-blue/green-waves-one.svg" class="w-full">
    </section>
</template>

<script>
export default {
    data() {
        return {
            title: 'Unieke website die bij jouw unieke bedrijf past',
            subtitle: 'De zakelijke website',
            content: 'Omdat ik een passie heb voor de online aanwezigheid van jouw bedrijf dat je met passie leidt. Mijn hart gaat sneller kloppen van een zakelijke website die me direct de ondernemer erachter laat zien en me vertelt  wat ik wil weten. Een heldere navigatie, aantrekkelijke foto’s en vooral een makkelijke én toegankelijke flow die jouw klant meeneemt op een reis door jouw bedrijf.'
        }
    }
}
</script>