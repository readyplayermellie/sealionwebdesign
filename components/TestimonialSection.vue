<template>
    <section id="testimonial-section">
        <div class="flex content-container">
            <div class="w-3/5">
                <div class="mb-6">
                    <h3>{{ subtitle }}</h3>
                    <h2>{{ title }}</h2>
                </div>
                <div>
                    <div class="rounded-lg card-border-pink p-6 testimonial-item">
                        <p class="mb-2">{{ testimonial.content }}</p>
                        <h4>{{ testimonial.customer }}</h4>
                    </div>
                </div>
            </div>
            <img src="~/assets/content/decoration/jellyfish-group.png" class="w-2/5">
        </div>
        <img src="~/assets/content/dividers/waves/Blue-to-sand/sand-waves-one.svg" class="w-full">
    </section>
</template>

<script>
export default {
    data() {
        return {
            title: 'Lovende woorden van happy ondernemers',
            subtitle: 'Zij gingen je voor',
            testimonial: {
                content: '\'Dankzij Melanie\'s expertise en toewijding is mijn bedrijf gegroeid van een idee tot een grote projectorganisatie. Haar bijdrage was essentieel in deze groei. Ik beveel Melanie ten zeerste aan voor iedereen die klaar is om de volgende stap te zetten, maar vastloopt op het gebied van webdesign en online vindbaarheid.\'',
                customer: 'De Bouwdirigent'
            },
        }
    },
}
</script>