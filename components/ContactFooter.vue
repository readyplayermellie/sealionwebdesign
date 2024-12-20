<template>
    <section id="contact-footer-section">
        <div class="content-container">
            <div class="mb-6">
                <a name="contact"></a>
                <h3>{{ sectionSubTitle }}</h3>
                <h2>{{ sectionTitle }}</h2>
            </div>
            <div class="flex">
                <!-- <ContactForm class="w-1/2"/> -->
                <p>Stuur een mailtje naar <a href="mailto:hello@sealionwebdesign.com" class="underline underline-offset-2">hello@sealionwebdesign.com</a></p>
            </div>
        </div>
        <img src="~/assets/content/dividers/waves/Sand-to-blue/green-waves-one.svg" class="w-screen">
    </section>
    <div id="footer-links-section" class="mb-20 pt-12">
        <FooterItems class="flex justify-between" id="general-footer"/>
    </div>
</template>

<script>
export default {
    data() {
        return {
            sectionTitle: 'Ik kijk ernaar uit van je te horen',
            sectionSubTitle: 'Benieuwd naar wat voor moois wij samen kunnen maken?'
        }
    }
}
</script>