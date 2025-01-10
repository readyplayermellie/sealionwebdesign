<template>
    <section class="pt-24 pb-40">
        <a name="questions"></a>
        <div class="container">
            <div class="flex justify-center flex-wrap">
                <div v-for="(item, index) in questionContent" :key="index" class="border border-white p-8 mt-12 m-2 relative md:max-w-72">
                    <img src="../assets/icons/wheel.png" alt="Icoon van een stuurwiel ter decoratie" class="w-12 h-12 absolute wheel-icon">
                    <h3 class="pt-8 text-xl pb-4">{{ item.question }}</h3>
                    <p>{{ item.content }}</p>
                </div>
            </div>
            <div class="text-center m-4">
                <h3 class="pb-4">{{ cta }}</h3>
                <a class="btn btn-primary md:w-80 max-w-80" href="#contact">{{ button }}</a>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            questionContent: [
                {
                    question: 'Ben je begonnen met jouw toffe bedrijf, maar kunnen klanten jou online nog niet vinden?',
                    content: 'Samen met jou zetten we binnen no-time een gebruiksvriendelijke, toegankelijke website op die jouw bedrijf perfect neerzet, zodat jouw klanten jou zonder problemen weten te vinden.'
                },
                {
                    question: 'Werkt jouw website wel op desktop, maar niet goed op mobiele apparaten?',
                    content: 'Anno 2025 een absolute no-go, natuurlijk. Daarom design ik elke website als eerste op mobiel, daarna op tablet en daarna op laptop. Een responsieve website die jouw klanten op alle apparaten kunnen benaderen.'
                },
                {
                    question: 'Kosten technische problemen op jouw website je veel tijd en stress?',
                    content: 'Je bent niet alleen! Problemen met de website kunnen erg veel tijd kosten en behoorlijk wat stress opleveren. Gelukkig zie ik technische problemen als technische puzzels die ik met wat aandacht oplos.'
                }
            ],
            cta: 'Vraag een gratis 30-minuten intake aan voor jouw nieuwe professionele website.',
            button: 'Boek een gratis intake'
        }
    }
}
</script>