<template>
    <section id="second-footer-section">
        <div class="content-container flex flex-col content-between">
            <div id="smaller-footer">
                <h3>{{ subtitle }}</h3>
                <h2 class="mb-20">{{ title }}</h2>
                <NuxtLink to="/#contact" class="btn btn-primary mt-8">Neem contact op</NuxtLink>
            </div>
        </div>
        <img src="~/assets/content/dividers/waves/Blue-to-sand/sand-waves-one.svg" class="w-full">
    </section>
    <div id="smaller-footer-section">
        <FooterItems class="flex justify-between pb-20 pt-12" id="smaller-footer-items"/>
    </div>
</template>

<script>
export default {
    data() {
        return {
            title: 'Samen een website maken?',
            subtitle: 'Vraag vrijblijvend een offerte op of plan een gratis 15-minuten intake in'
        }
    }
}
</script>