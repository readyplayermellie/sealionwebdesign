<template>
    <section id="hero-section" class="text-center">
        <div class="content-container">
            <h1 class="mt-24">{{ sectionTitle }}</h1>
            <h2 id="hero-subtitle" class="mb-8">{{ sectionSubTitle }}</h2>
            <a class="btn btn-primary mt-8" href="/#services">{{ buttonText }}</a>
        </div>
        <img src="~/assets/content/dividers/waves/Blue-to-sand/sand-waves-one.svg" class="w-full">
    </section>
</template>

<script>
export default {
    data() {
        return {
            sectionTitle: 'Jouw zakelijke website met een spark',
            sectionSubTitle: 'Unieke zakelijke websites voor de ondernemer met passie',
            buttonText: 'Zo\'n website wil ik wel'
        }
    }
}
</script>