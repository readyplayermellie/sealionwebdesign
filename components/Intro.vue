<template>
    <section id="intro">
        <div class="text-center intro-title">
            <h3>{{ subtitle }}</h3>
            <h2>{{ title }}</h2>
        </div>
        <div id="intro-content">
            <div class="flex justify-center items-center mb-14" v-for="(item, index) in contentItems" :key="index">
                <img v-if="item.left" src="/assets/content/bubble.png" class="h-36 item-img-left bubbles hidden lg:block">
                <div class="w-64 text-center lg:text-left">
                    <h4 class="intro-item-title">{{ item.title }}</h4>
                    <p>{{ item.text }}</p>
                </div>
                <img v-if="!item.left" src="/assets/content/bubble.png" class="h-36 bubbles hidden lg:block">
            </div>
        </div>
        <div class="text-center">
            <h4>Sea Lion Web Design werkt hard aan een positieve impact op de wereld.</h4>
            <p>Naast de bewuste keuzes tijdens de websiteontwikkeling, doneer ik elk jaar 5% van mijn inkomsten aan een goed doel. In 2024 is dit:</p>
            <a href="https://www.dierenambulance-amsterdam.nl/" target="_blank" class="group flex py-8 inline-block justify-center dieren-link">
                <img src="/assets/content/arrow.png" class="mr-2 group-hover:ml-2 arrows">
                <span>Dierenambulance Amsterdam</span>
            </a>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            title: 'SEA LION WEB DESIGN',
            subtitle: 'HOE IK INDRUK EN IMPACT MAAK MET',
            contentItems: [
                {
                    title: 'HET WEB',
                    text: 'Mooie, doordachte websites met een handige CMS voor al je content of juist een duidelijke landingspagina met een kort contactformulier. Iedere website komt met eigen wensen, een eigen design en een eigen aanpak. Toch hebben ze allemaal wat gemeen: toegankelijk voor iedereen en elk apparaat en gebouwd met het oog op de toekomst.',
                    left: false
                },
                {
                    title: 'DEVELOPER IN HART EN NIEREN',
                    text: 'Van goedwerkende applicaties bedenken en maken tot mensen helpen met het oplossen van software-uitdagingen. Ik doe (bijna) niets liever dan met mijn neus in de code duiken. Als gepassioneerde developer denk ik graag mee met de uitdagingen waar je voor staat.',
                    left: true
                },
                {
                    title: 'DUURZAAM',
                    text: 'Op een duurzamere manier websites bouwen en technologie gebruiken, dat is waar Sea Lion Web Design voor staat. Geen grote complexe website bouwen als de situatie vraagt om een simpele, maar effectieve pagina.Een groenere hostingpartij kiezen. Het energieverbruik van een website onder controle houden. Kleine bewegingen met groot effect.',
                    left: false
                }
            ]
        }
    }
}
</script>

<style scoped>
.item-img-left {
    transform: rotate(180deg);
}

#intro-content {
    margin-bottom: 150px;
}

.intro-title {
    margin-top: 100px;
    margin-bottom: 100px;
}

.bubbles {
    margin-left: 150px;
    margin-right: 150px;
}

.dieren-link:hover {
    border: none;
}
</style>