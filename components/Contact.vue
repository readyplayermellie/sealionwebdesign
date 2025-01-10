<template>
        <section class="pt-40 pb-40" id="contact-section">
            <a name="contact"></a>
            <div class="container">
                <h2 class="pb-4 text-3xl">{{ title }}</h2>
                <p class="pb-2">{{ subtitle }}</p>
                <p v-for="(item, index) in content" :key="index" class="pb-2">{{ item }}</p>
                <a href="mailto:hello@sealionwebdesign.com" target="_blank" class="flex items-center mt-8">
                    <img src="../assets/icons/mail.png" class="mr-4 w-6 h-6">
                    <span>hello@sealionwebdesign.com</span>
                </a>
            </div>
        </section>
</template>

<script>
export default {
    data() {
        return {
            title: 'Neem contact met me op',
            subtitle: 'Zodat wij morgen al aan jouw nieuwe professionele website kunnen werken.',
            content: [
                'In een gratis intake die 30 minuten duurt, vertel jij mij wat je zoekt en kijk ik samen met jou naar de mogelijkheden.',
                'Staat jouw wens niet op de website? Ook dan krijg ik graag jouw bericht. Ik hou van uitdagingen!',
            ],
        }
    }
}
</script>