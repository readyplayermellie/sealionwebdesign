<template>
    <section id="about-section">
        <div class="content-container">
            <div class="mb-20">
                <h3>{{ subtitle }}</h3>
                <h2>{{ title }}</h2>
            </div>
            <div class="flex mb-20">
                <img src="~/assets/content/decoration/seal.jpg" class="rounded-lg w-1/3">
                <p class="pl-4">{{ content }}</p>
            </div>
        </div>
        <img src="~/assets/content/dividers/waves/Sand-to-blue/green-waves-one.svg" class="w-full">
    </section>
</template>

<script>
export default {
    data() {
        return {
            title: 'De meid achter Sea Lion Web Design',
            subtitle: 'Front-end developer met hart en ziel',
            content: 'Websites maken en software bouwen vind ik fantastisch. Vooral als ik met mijn creaties een positieve impact op de maatschappij en de wereld om ons heen kan hebben. Al 5+ jaar groei ik met veel plezier en ambitie als front-end developer binnen de financiële sector en is mijn kennis in onder andere Vue.js, Nuxt.js, Node.js en Lit onwijs gegroeid. Sea Lion Web Design is ontstaan uit een behoefte naar autonomie en als grote creatieve uitspatting, vanuit het gevoel dat ik als mens en als ondernemer technologie op een duurzamere manier kan gebruiken om andere ondernemers op die manier te ondersteunen.'
        }
    }
}
</script>