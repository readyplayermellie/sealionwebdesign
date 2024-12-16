<template>
    <section id="more-testimonials-section">
        <div class="content-container">
            <div>
                <div class="mb-6">
                    <h3>{{ title }}</h3>
                    <h2>{{ subtitle }}</h2>
                </div>
                <div>
                    <div class="rounded-lg card-border-blue p-6 testimonial-item" id="first-testimonial">
                        <p class="mb-2">{{ firstTestimonial.content }}</p>
                        <h4>{{ firstTestimonial.customer }}</h4>
                    </div>
                </div>
            </div>
        </div>
        <img src="../assets/content/dividers/waves/Pink-to-blue/blue-waves-one.svg" class="w-full">
    </section>
</template>

<script>
export default {
    data() {
        return {
            title: 'Woorden waar ik trots op ben',
            subtitle: 'Nog meer tevreden ondernemers',
            firstTestimonial: {
                content: '\'Melanie heeft op een professionele manier gewerkt om een vervelend issue op mijn website te verhelpen en alle updates gedaan die nodig waren om de website weer op alle fronten up-to-date te krijgen. Ze heeft door haar creativiteit te gebruiken een oplossing gevonden om het issue te verhelpen waar ik al maanden mee zat. Daarnaast heeft ze er ook nog eens gezorgd dat mijn back-ups weer netjes verlopen en advies gegeven over de vervolgstappen voor mijn website. Melanies doorzettingsvermogen en haar meedenkende dienstverlening zorgen er voor dat ik het iedereen kan aanraden om met Sea Lion Web Design in zee te gaan!\'',
                customer: 'Joost'
            },
        }
    }
}
</script>