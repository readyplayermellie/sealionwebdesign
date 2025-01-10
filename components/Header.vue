<template>
    <div class="h-screen" id="header">
        <NavBar />
        <div class="h-5/6 flex flex-col justify-center text-center p-4 items-center relative">
            <h1 class="text-5xl md:text-6xl max-w-3xl">{{ title }}</h1>
            <h2 class="text-2xl mt-4" id="subtitle">{{ subtitle }}</h2>
            <div class="flex flex-col lg:flex-row mt-8">
                <a href="#contact" class="btn btn-primary mt-8 mb-2 lg:mb-0 lg:mt-0 w-80 lg:mr-2">{{ primaryButton }}</a>
                <a href="#diensten" class="btn btn-secondary w-80">{{ secondaryButton }}</a>
            </div>
            <a href="/#questions">
                <img src="../assets/icons/anchor-icon.png" :alt="iconAlt" class="h-12 w-12 absolute bottom-5" id="anchor-icon">
            </a>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            title: 'Jouw zakelijke website die de diepte in gaat',
            subtitle: 'Unieke zakelijke websites voor de ondernemer met passie',
            primaryButton: 'Boek een gratis intake',
            secondaryButton: 'Meer over jouw nieuwe website',
            iconAlt: 'Anker icoon om te laten zien dat je naar beneden moet scrollen voor meer content'
        }
    }
}
</script>